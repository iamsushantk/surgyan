<script>
	import Swar from './Swar.svelte';
	const swars = 'D-.N-.S.R.G.M.P.D.N.S+.R+.G+'.split('.');
</script>

<div class="swars">
	{#each swars as swar}
		<Swar {swar} />
	{/each}
</div>

<style scoped>
	.swars {
		display: flex;
		flex-wrap: wrap;
		gap: var(--space-xxx);
		justify-content: center;
	}
</style>
