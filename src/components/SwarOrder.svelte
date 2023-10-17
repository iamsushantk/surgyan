<script>
	export let name;
	export let pattern;
	const tokens = pattern.split('/') || [];
</script>

<div class="swar-order">
	<div class="swar-order__name">
		{name}
	</div>
	<div class="swar-order__tokens">
		{#each tokens as token}
			<div class="swar-order__token">
				{token}
			</div>
		{/each}
	</div>
</div>

<style scoped>
	.swar-order {
		display: flex;
		gap: var(--space-xx);
		padding: var(--space-xx);
		border: var(--border-x) solid pink;
	}

	.swar-order__name {
		display: flex;
		font-weight: bold;
		place-items: center;
		background-color: pink;
	}

	.swar-order__name,
	.swar-order__tokens {
		padding: var(--space-xx);
	}

	.swar-order__tokens {
		display: flex;
		flex-wrap: wrap;
		gap: var(--space-xx);
	}

	.swar-order__token {
		flex-grow: 1;
		text-align: center;
		padding: var(--space-x);
		border: var(--border-x) solid pink;
	}
</style>
