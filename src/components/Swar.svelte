<script>
	import Div from './Div.svelte';
	import Audio from './Audio.svelte';

	export let swar;
	const getSwarUrl = (swar) => `/data/media/swars/${swar}.mp3`;
</script>

<Div className={'bg-pink-300'}>
	<Audio trackName={swar} trackUrl={`${getSwarUrl(swar)}`} />
</Div>
