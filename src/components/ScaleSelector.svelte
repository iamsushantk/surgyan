<script>
	import axios from 'axios';
	import { onMount } from 'svelte';
	import Icon from './Icon.svelte';
	import Constants from '../constants';

	let scales = [];
	let activeScale = null;
	let audioControl = null;
	let audioIsPlaying = false;

	onMount(async () => {
		audioControl.onpause = () => (audioIsPlaying = false);
		audioControl.onplaying = () => (audioIsPlaying = true);
		scales = (await axios.get(`${Constants.dbBaseUrl}/tanpura-scales.json`))?.data || [];
	});

	const onAudioClick = () => {
		!audioIsPlaying ? audioControl.play() : audioControl.pause();
	};

	const onScaleSelect = (scale) => {
		activeScale = scale;
		audioIsPlaying = false;
	};
</script>

<div class="input-group d-flex justify-content-center">
	<button
		data-bs-toggle="dropdown"
		class="btn btn-primary dropdown-toggle"
	>
		{!activeScale ? 'Choose scale' : 'Change Scale'}
	</button>
	<ul class="dropdown-menu">
		{#each scales as scale}
			<li>
				<a
					class="dropdown-item"
					on:click={() => onScaleSelect(scale)}
				>
					{scale.name}
				</a>
			</li>
		{/each}
	</ul>
	<div class="input-group-text form-control d-flex justify-content-center text-warning">
		{activeScale ? `Scale ${activeScale.name} selected` : '-'}
	</div>
	<button
		on:click={onAudioClick}
		class:disabled={!activeScale}
		class="btn btn-outline-primary"
	>
		<Icon name={!audioIsPlaying ? 'play' : 'pause'} />
	</button>
	<audio
		bind:this={audioControl}
		class="form-control"
		src={`${Constants.dbBaseUrl}/${activeScale?.mediaUrl}`}
	/>
</div>
