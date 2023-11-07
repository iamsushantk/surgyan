<script>
	import Section from './Section.svelte';

	export let type;
	export let pattern;
	const swarGroups = pattern.split('/') || [];
</script>

<Section className={'flex gap-1 border-solid border-2 border-pink-500'}>
	<Section className={'type p-1 flex bg-pink-600 text-white font-bold place-items-center'}>
		{type}
	</Section>
	<Section className={'p-1 flex w-full flex-wrap gap-1'}>
		{#each swarGroups as swarGroup}
			<Section className={'p-0.5 grow bg-pink-200 text-center border-solid border-2 border-pink-600'}>
				{swarGroup}
			</Section>
		{/each}
	</Section>
</Section>
