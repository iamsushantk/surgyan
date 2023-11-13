<script>
	import axios from 'axios';
	import { onMount } from 'svelte';

	import Constants from '../constants';
	import FontIcon from './FontIcon.svelte';

	let scales = [];
	let activeScale = null;
	let audioControl = null;
	let isAudioPlaying = false;

	onMount(async () => {
		audioControl.onpause = () => (isAudioPlaying = false);
		audioControl.onplaying = () => (isAudioPlaying = true);
		scales = (await axios.get(`${Constants.dbBaseUrl}/tanpura-scales.json`))?.data || [];
	});

	const onAudioActivated = () => {
		!isAudioPlaying ? audioControl?.play() : audioControl?.pause();
	};
</script>

<section class="input-group d-flex justify-content-center">
	<button class="btn btn-primary dropdown-toggle" type="button" data-bs-toggle="dropdown">
		<span>Choose Scale</span>
	</button>
	<ul class="dropdown-menu">
		{#each scales as scale}
			<li>
				<a
					class="dropdown-item"
					on:click={() => {
						activeScale = scale;
						isAudioPlaying = false;
					}}>{scale.name}</a
				>
			</li>
		{/each}
	</ul>
	<span class="input-group-text">{activeScale?.name ?? '-'}</span>
	<button
		class="btn btn-outline-primary"
		class:invisible={!activeScale}
		class:disabled={!activeScale}
		on:click={onAudioActivated}><FontIcon name={!isAudioPlaying ? 'play' : 'pause'} /></button
	>
	<audio
		bind:this={audioControl}
		class="form-control"
		src={`${Constants.dbBaseUrl}/${activeScale?.mediaUrl}`}
	/>
</section>

<style>
	audio {
		border: 1px solid red;
	}
</style>
