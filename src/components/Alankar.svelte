<script>
	export let alankar;
	import Audio from './Audio.svelte';
	import SwarSequence from './SwarSequence.svelte';
</script>

<div class="flex gap-1 flex-col">
	<div class="font-bold bg-indigo-800 text-white text-center p-1">
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
