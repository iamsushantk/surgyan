<script>
	import Audio from './Audio.svelte';
	import Section from './Section.svelte';

	export let swar;
	const getSwarUrl = (swar) => `/data/media/swars/${swar}.mp3`;
</script>

<Section className={'bg-pink-300'}>
	<Audio trackName={swar} trackUrl={`${getSwarUrl(swar)}`} />
</Section>
