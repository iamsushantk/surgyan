<script>
	import Div from './Div.svelte';

	export let type;
	export let pattern;
	const swarGroups = pattern.split('/') || [];
</script>

<Div className={'flex gap-1 border-solid border-2 border-pink-500'}>
	<Div className={'type p-1 flex bg-pink-600 text-white font-bold place-items-center'}>
		{type}
	</Div>
	<Div className={'p-1 flex w-full flex-wrap gap-1'}>
		{#each swarGroups as swarGroup}
			<Div className={'p-0.5 grow border-solid border-2 border-pink-300 text-center'}>
				{swarGroup}
			</Div>
		{/each}
	</Div>
</Div>
