<script>
	import axios from 'axios';
	import { onMount } from 'svelte';

	import Constants from '../constants';

	let alankarLessons = [];

	onMount(async () => {
		alankarLessons = (await axios.get(`${Constants.dbBaseUrl}/alankars.json`))?.data || [];
	});
</script>

<div class="d-flex gap-3 m-2 flex-wrap">
	{#each alankarLessons as alankarLesson}
		<div class="card flex-grow-1">
			<div class="card-header">{alankarLesson.name}</div>
			<div class="card-body">
				<a href={`/lessons/alankars/${alankarLesson.id}`} class="btn btn-primary">Go to Lesson</a>
			</div>
		</div>
	{/each}
</div>
