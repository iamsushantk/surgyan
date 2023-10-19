<script>
	import lessons from '../data/lessons';

	import Div from './Div.svelte';
	import Swar from './Swar.svelte';
	import Lesson from './Lesson.svelte';

	const swars = 'D-.N-.S.R.G.M.P.D.N.S+.R+.G+'.split('.');
</script>

<Div className={'flex flex-col gap-1 p-2'}>
	<Div className={'flex flex-col gap-2'}>
		{#each lessons as lesson}
			<Lesson {lesson} />
		{/each}
	</Div>
</Div>
