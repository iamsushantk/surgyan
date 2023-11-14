<script>
	import { lessonStore } from '../../../../store';
	import Lesson from '../../../../components/Lesson.svelte';

	export let data;
	let activeLesson = null;

	lessonStore.subscribe((lessons) => (activeLesson = lessons.find((l) => l.id === data.slug)));
</script>

{#if activeLesson}
	<Lesson lesson={activeLesson} />
{/if}
