<script>
	import Div from './Div.svelte';
	import Alankar from './Alankar.svelte';

	export let lesson;
</script>

<Div className={'flex gap-2 border-solid border-0 border-pink-600 flex-col'}>
	<Div className={'p-4 font-bold text-center bg-pink-600 text-white'}>{lesson.name}</Div>
	{#each lesson.alankars as alankar}
		<Alankar {alankar} />
	{/each}
</Div>
