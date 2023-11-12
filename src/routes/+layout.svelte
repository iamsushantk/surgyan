<script>
	import '../styles/index.css';
	import ScaleSelector from '../components/ScaleSelector.svelte';
</script>

<nav class="navbar navbar-expand-sm navbar-dark bg-dark">
	<section class="container-fluid">
		<a class="navbar-brand" href="/">surgyan</a>
		<div class="navbar-collapse">
			<ul class="navbar-nav">
				<li class="nav-item">
					<a class="nav-link active" href="/">Home</a>
				</li>
			</ul>
		</div>
	</section>
</nav>
<section class="p-2">
	<ScaleSelector />
</section>
<slot />
<nav class="navbar fixed-bottom navbar-dark bg-dark">
	<section class="container-fluid" />
</nav>
