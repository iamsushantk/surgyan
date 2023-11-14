<script>
	export let alankar;

	import Constants from '../constants';
	import SwarSequence from './SwarSequence.svelte';

	$: mediaUrl = `${Constants.dbBaseUrl}/${alankar.mediaUrl}`;
</script>

<div class="d-flex flex-column gap-2">
	{#if alankar.mediaUrl}
		<div class="card">
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
</div>
