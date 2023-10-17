<script>
	export let swar;
	import Audio from './Audio.svelte';
	const getSwarUrl = (swar) => `/data/media/swars/${swar}.mp3`;
</script>

<div class="swar">
	<Audio trackName={swar} trackUrl={`${getSwarUrl(swar)}`} />
</div>

<style scoped>
	.swar {
		padding: 5px;
		color: white;
		min-width: 120px;
		background-color: rgb(49, 47, 47);
	}
</style>
