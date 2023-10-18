<script>
	export let alankar;
	import Audio from './Audio.svelte';
	import SwarSequence from './SwarSequence.svelte';
</script>

<div class="alankar">
	<div class="header">
		{'#' + alankar.id}
	</div>
	{#if alankar.mediaUrl}
		<div class="audio">
			<Audio trackName="" trackUrl={alankar.mediaUrl} />
		</div>
	{/if}
	<SwarSequence type="Aaroh" pattern={alankar.aaroh} />
	<SwarSequence type="Avroh" pattern={alankar.avroh} />
</div>

<style scoped>
	.alankar {
		display: flex;
		gap: var(--space-xx);
		flex-direction: column;
		border-bottom: 5px solid red;
	}

	.alankar > .header {
		font-weight: bold;
		text-align: center;
		padding: var(--space-xx);
		background-color: pink;
	}

	.alankar > .audio {
		display: flex;
		justify-content: center;
	}
</style>
