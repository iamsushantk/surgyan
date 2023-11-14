<script>
	import { onMount } from 'svelte';
	import { lessonStore } from '../store';

	let alankarLessons = [];
	lessonStore.subscribe((lessons) => (alankarLessons = lessons || []));
</script>

<div class="d-flex flex-wrap gap-3 m-2">
	{#each alankarLessons as alankarLesson}
		<div class="card flex-grow-1">
			<div class="card-header">
				{alankarLesson.name}
			</div>
			<div class="card-body">
				<a
					class="btn btn-primary"
					href={`/lessons/alankars/${alankarLesson.id}`}
				>
					Go to Lesson
				</a>
			</div>
		</div>
	{/each}
</div>
