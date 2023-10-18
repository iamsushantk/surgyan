<script>
	export let trackUrl;
	export let trackName;
	const playAudio = (e) => e.target.parentElement.querySelector('audio')?.play();
	const pauseAudio = (e) => e.target.parentElement.querySelector('audio')?.pause();
</script>

<div class="border-solid border-2 border-indigo-200 p-1 flex justify-evenly place-items-center gap-1">
	<audio src={trackUrl} />
	{#if trackName}
		<div class="font-bold">{trackName}</div>
	{/if}
	<button
		type="button"
		class="border-0 bg-indigo-800 p-2 text-white fa fa-play"
		on:click={playAudio}
	/>
	<button
		type="button"
		class="border-0 bg-indigo-800 p-2 text-white fa fa-pause"
		on:click={pauseAudio}
	/>
</div>
