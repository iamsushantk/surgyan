<script>
	export let alankar;

	import Audio from './Audio.svelte';
	import Div from './Div.svelte';
	import SwarSequence from './SwarSequence.svelte';
</script>

<Div className={'flex gap-2 flex-col border-solid border-2 border-pink-600 p-2'}>
	<Div className={'font-bold bg-pink-600 rounded text-white text-center p-1'}>
		{'#' + alankar.id}
	</Div>
	{#if alankar.mediaUrl}
		<Div className={'flex justify-center border-solid border-2 border-pink-500'}>
			<Audio src={alankar.mediaUrl} />
		</Div>
	{/if}
	<SwarSequence type="Aaroh" pattern={alankar.aaroh} />
	<SwarSequence type="Avroh" pattern={alankar.avroh} />
</Div>
