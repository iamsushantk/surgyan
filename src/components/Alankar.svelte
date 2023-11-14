<script>
	export let alankar;

	import Constants from '../constants';
	import SwarSequence from './SwarSequence.svelte';

	$: mediaUrl = `${Constants.dbBaseUrl}/${alankar.mediaUrl}`;
</script>

<section>
	{#if alankar.mediaUrl}
		<div class="card mb-2">
			<div class="card-header">Audio Recording</div>
			<div class="card-body">
				<audio
					class="w-100"
					controls
					src={mediaUrl}
				/>
			</div>
		</div>
	{/if}
	<SwarSequence
		type="Aaroh"
		pattern={alankar.aaroh}
	/>
	<SwarSequence
		type="Avroh"
		pattern={alankar.avroh}
	/>
</section>
