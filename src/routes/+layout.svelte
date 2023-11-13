<script>
	import '../styles/index.css';
	import ScaleSelector from '../components/ScaleSelector.svelte';
</script>

<nav class="navbar navbar-expand-sm navbar-dark bg-dark">
	<section class="container-fluid">
		<a class="navbar-brand" href="/">surgyan</a>
	</section>
</nav>
<section class="p-2">
	<ScaleSelector />
</section>
<slot />
<nav class="navbar fixed-bottom navbar-dark bg-dark">
	<section class="container-fluid" />
</nav>
