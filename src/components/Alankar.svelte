<script>
	export let alankar;
	import Audio from './Audio.svelte';
	import SwarSequence from './SwarSequence.svelte';
</script>

<div class="flex gap-2 flex-col border-solid border-2 border-indigo-800 p-2">
	<div class="font-bold bg-indigo-800 rounded text-white text-center p-1">
		{'#' + alankar.id}
	</div>
	{#if alankar.mediaUrl}
		<div class="flex justify-center">
			<Audio trackName="" trackUrl={alankar.mediaUrl} />
		</div>
	{/if}
	<SwarSequence type="Aaroh" pattern={alankar.aaroh} />
	<SwarSequence type="Avroh" pattern={alankar.avroh} />
</div>
