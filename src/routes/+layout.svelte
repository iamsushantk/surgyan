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
		<section class="container-fluid">
			<a
				href="/"
				class="navbar-brand"
			>
				surgyan
			</a>
		</section>
	</nav>
</header>
<main>
	<section class="p-2 border-bottom">
		<ScaleSelector />
	</section>
	<slot />
</main>
<footer>
	<nav class="navbar fixed-bottom navbar-dark bg-dark">
		<section class="container-fluid" />
	</nav>
</footer>
