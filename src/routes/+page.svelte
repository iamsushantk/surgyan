<script>
	import { onMount } from 'svelte';
	import { lessonStore } from '../store';

	let alankarLessons = [];
	lessonStore.subscribe((lessons) => (alankarLessons = lessons || []));
</script>

<div class="d-flex gap-2 flex-column">
	{#each alankarLessons as alankarLesson}
		<div class="card">
			<div class="card-header text-white">
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