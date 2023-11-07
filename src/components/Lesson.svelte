<script>
	import Section from './Section.svelte';
	import Alankar from './Alankar.svelte';

	export let lesson;
</script>

<Section className={'flex gap-2 border-pink-600 flex-col'}>
	<Section className={'p-2 font-bold text-center rounded-t bg-pink-800 text-white'}>{lesson.name}</Section>
	{#each lesson.alankars as alankar}
		<Alankar {alankar} />
	{/each}
</Section>
