<script>
	import axios from 'axios';
	import { onMount } from 'svelte';

	import Audio from './Audio.svelte';
	import Constants from '../constants';

	let scales = [];
	let activeScale = null;

	onMount(async () => {
		scales = (await axios.get(`${Constants.dbBaseUrl}/tanpura-scales.json`))?.data || [];
	});
</script>

<section class="input-group">
	<button class="btn btn-success dropdown-toggle" type="button" data-bs-toggle="dropdown"
		>Choose Scale</button
	>
	<ul class="dropdown-menu">
		{#each scales as scale}
			<li>
				<a class="dropdown-item" href="#" on:click={() => (activeScale = scale)}>{scale.name}</a>
			</li>
		{/each}
	</ul>
	<span class="input-group-text">{activeScale?.name ?? '-'}</span>
	<Audio className="form-control" src={`${Constants.dbBaseUrl}/${activeScale?.mediaUrl}`} />
</section>
