<script>
	import lessons from '../data/lessons';
	import Swar from './Swar.svelte';
	import Lesson from './Lesson.svelte';

	const swars = 'D-.N-.S.R.G.M.P.D.N.S+.R+.G+'.split('.');
</script>

<div class="flex flex-col gap-1 p-2">
	<div class="sticky top-0 flex flex-wrap justify-center gap-2 bg-indigo-200">
		{#each swars as swar}
			<Swar {swar} />
		{/each}
	</div>
	<div class="flex flex-col gap-2">
		{#each lessons as lesson}
			<Lesson {lesson} />
		{/each}
	</div>
</div>
