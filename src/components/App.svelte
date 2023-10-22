<script>
	import axios from 'axios';
	import { onMount } from 'svelte';

	import Constants from '../constants';
	import Lesson from './Lesson.svelte';
	import Section from './Section.svelte';

	let lessons = [];

	onMount(async () => {
		lessons = (await axios.get(`${Constants.baseUrl}/lessons.json`))?.data || [];
	});
</script>

<Section className={'flex flex-col gap-1 p-2'}>
	<Section className={'flex flex-col gap-2'}>
		{#each lessons as lesson}
			<Lesson {lesson} />
		{/each}
	</Section>
</Section>
