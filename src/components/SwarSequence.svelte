<script>
	export let type;
	export let pattern;
	const swarGroups = pattern.split('/') || [];
</script>

<div class="card mt-2">
	<div class="card-header">{type}</div>
	<div class="card-body">
		<div class="list-group d-flex flex-row flex-wrap gap-2">
			{#each swarGroups as swarGroup}
				<span
					type="button"
					class="btn btn-primary flex-grow-1 my-2">{swarGroup}</span
				>
			{/each}
		</div>
	</div>
</div>
