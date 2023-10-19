<script>
	import lessons from '../data/lessons';

	import Swar from './Swar.svelte';
	import Lesson from './Lesson.svelte';
	import Section from './Section.svelte';

	const swars = 'D-.N-.S.R.G.M.P.D.N.S+.R+.G+'.split('.');
</script>

<Section className={'flex flex-col gap-1 p-2'}>
	<Section className={'flex flex-col gap-2'}>
		{#each lessons as lesson}
			<Lesson {lesson} />
		{/each}
	</Section>
</Section>
