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
		gap: 5px;
		padding: 5px;
		display: flex;
		border: 2px solid pink;
	}

	.swar-order__name {
		display: flex;
        font-weight: bold;
		place-items: center;
		background-color: pink;
	}

	.swar-order__name,
	.swar-order__tokens {
		padding: 8px;
	}

	.swar-order__tokens {
		gap: 5px;
		display: flex;
		flex-wrap: wrap;
	}

	.swar-order__token {
		padding: 5px;
		text-align: center;
		border: 2px solid pink;
		text-decoration: underline;
	}
</style>
