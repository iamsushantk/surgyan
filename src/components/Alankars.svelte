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
		gap: 5px;
		display: flex;
		flex-direction: column;
	}
</style>
