<script>
	export let trackUrl;
	export let trackName;
	const playAudio = (e) => e.target.parentElement.querySelector('audio')?.play();
	const pauseAudio = (e) => e.target.parentElement.querySelector('audio')?.pause();
</script>

<div class="audio">
	<audio src={trackUrl} />
	{#if trackName}
		<div class="name">{trackName}</div>
	{/if}
	<button type="button" class="control fa fa-play" on:click={playAudio} />
	<button type="button" class="control fa fa-pause" on:click={pauseAudio} />
</div>

<style scoped>
	.audio {
		display: flex;
		align-items: center;
		gap: var(--space-xx);
		padding: var(--space-xx);
		justify-content: space-evenly;
		border: var(--border-xx) solid pink;
	}

	.audio > .name {
		font-weight: bold;
	}

	.audio > .control {
		border: none;
		cursor: pointer;
		padding: var(--space-xx);
		background-color: pink;
	}

	.control:hover {
		background-color: lightcoral;
	}
</style>
