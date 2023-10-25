<script>
	export let alankar;

	import Constants from '../constants';

	import Audio from './Audio.svelte';
	import Section from './Section.svelte';
	import SwarSequence from './SwarSequence.svelte';

	$: mediaUrl = `${Constants.dbBaseUrl}/${alankar.mediaUrl}`;
</script>

<Section className={'flex gap-2 flex-col border-solid border-0 border-pink-600'}>
	<Section
		className={'font-bold bg-pink-600 rounded-tl-full rounded-tr-full text-white text-center p-1'}
	>
		{'#' + alankar.id}
	</Section>
	{#if alankar.mediaUrl}
		<Section className={'flex justify-center rounded-[30px] border-solid border-2 border-pink-500'}>
			<Audio src={mediaUrl} className={'w-full h-6'} />
		</Section>
	{/if}
	<SwarSequence type="Aaroh" pattern={alankar.aaroh} />
	<SwarSequence type="Avroh" pattern={alankar.avroh} />
</Section>
