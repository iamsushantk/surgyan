<script>
	export let type;
	export let pattern;
	const swarGroups = pattern.split('/') || [];
</script>

<div class="flex gap-1 border-solid border-2">
	<div class="type p-1 flex bg-indigo-800 text-white font-bold place-items-center">
		{type}
	</div>
	<div class="p-1 flex flex-wrap gap-1">
		{#each swarGroups as swarGroup}
			<div class="p-0.5 grow border-solid border-2 border-indigo-300 text-center">
				{swarGroup}
			</div>
		{/each}
	</div>
</div>
