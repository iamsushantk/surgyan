<script>
	export let alankar;
	import Audio from './Audio.svelte';
	import SwarOrder from './SwarOrder.svelte';
</script>

<div class="alankar">
	<div class="alankar__header">
		{'#' + alankar.id}
	</div>
	{#if alankar.mediaUrl}
		<div class="alankar__audio">
			<Audio trackName="" trackUrl={alankar.mediaUrl} />
		</div>
	{/if}
	<div class="alankar__aaroh">
		<SwarOrder name="Aaroh" pattern={alankar.aaroh} />
	</div>
	<div class="alankar__avroh">
		<SwarOrder name="Avroh" pattern={alankar.avroh} />
	</div>
</div>

<style scoped>
	.alankar {
		gap: 5px;
		display: flex;
		flex-direction: column;
        border-bottom: 5px solid red;
	}

	.alankar__header {
		padding: 5px;
		font-weight: bold;
		text-align: center;
		background-color: pink;
	}

	.alankar__audio {
		display: flex;
		justify-content: center;
	}
</style>
