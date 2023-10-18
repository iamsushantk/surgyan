<script>
	export let type;
	export let pattern;
	const swarGroups = pattern.split('/') || [];
</script>

<div class="swar-sequence">
	<div class="type">
		{type}
	</div>
	<div class="swar-groups">
		{#each swarGroups as swarGroup}
			<div class="swar-group">
				{swarGroup}
			</div>
		{/each}
	</div>
</div>

<style scoped>
	.swar-sequence {
		display: flex;
		gap: var(--space-xx);
		padding: var(--space-xx);
		border: var(--border-x) solid pink;
	}

	.swar-sequence > .type {
		display: flex;
		font-weight: bold;
		place-items: center;
		background-color: pink;
	}

	.swar-sequence > .type,
	.swar-sequence > .swar-groups {
		padding: var(--space-xx);
	}

	.swar-sequence > .swar-groups {
		display: flex;
		flex-wrap: wrap;
		gap: var(--space-xx);
	}

	.swar-sequence > .swar-groups > .swar-group {
		flex-grow: 1;
		text-align: center;
		padding: var(--space-x);
		border: var(--border-x) solid pink;
	}
</style>
