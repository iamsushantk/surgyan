<script>
	export let alankars;
	import Alankar from './Alankar.svelte';
</script>

<div class="alankars">
	{#each alankars as alankar}
		<Alankar {alankar} />
	{/each}
</div>

<style scoped>
	.alankars {
		display: flex;
		gap: var(--space-xx);
		flex-direction: column;
	}
</style>
