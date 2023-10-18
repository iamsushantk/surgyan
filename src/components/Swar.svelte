<script>
	export let swar;
	import Audio from './Audio.svelte';
	const getSwarUrl = (swar) => `/data/media/swars/${swar}.mp3`;
</script>

<div class="bg-indigo-300">
	<Audio trackName={swar} trackUrl={`${getSwarUrl(swar)}`} />
</div>
