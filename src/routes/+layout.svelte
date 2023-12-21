<script>
	import '../styles/index.css';
	import axios from 'axios';
	import { onMount } from 'svelte';

	import { lessonStore } from '../store';
	import Constants from '../constants';
	import ScaleSelector from '../components/ScaleSelector.svelte';

	let alankarLessons = [];

	onMount(async () => {
		alankarLessons = (await axios.get(`${Constants.dbBaseUrl}/alankars.json`))?.data || [];
		lessonStore.set(alankarLessons);
	});
</script>

<header>
	<nav class="navbar navbar-expand-sm navbar-dark bg-dark">
		<div class="container-fluid">
			<a
				href="/"
				class="navbar-brand"
			>
				SurGyan
			</a>
		</div>
	</nav>
</header>
<main class="p-2 d-flex flex-column gap-2">
	<ScaleSelector/>
	<slot />
</main>
