<script>
	export let trackUrl;
	export let trackName;
	const playAudio = (e) => e.target.parentElement.querySelector('audio')?.play();
	const pauseAudio = (e) => e.target.parentElement.querySelector('audio')?.pause();
</script>

<div class="audio">
	<audio src={trackUrl} />
	<div class="audio__name">{trackName}</div>
	<button class="audio__control fa fa-play" on:click={playAudio}></button>
	<button class="audio__control fa fa-pause" on:click={pauseAudio}></button>
</div>

<style scoped>
	.audio {
		gap: 5px;
		padding: 5px;
		display: flex;
		align-items: center;
		justify-content: space-evenly;
		border: 2px solid pink;
	}

	.audio__name {
		font-weight: bold;
	}

	.audio__control {
		padding: 5px;
		cursor: pointer;
		background-color: pink;
	}
</style>
