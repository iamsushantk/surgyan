<script>
	import lessons from '../data/lessons';

	import Swars from './Swars.svelte';
	import Lessons from './Lessons.svelte';
</script>

<div class="app">
	<div class="app__header">Alankars</div>
	<div class="app__content">
		<div class="app__content-swars">
			<Swars />
		</div>
		<div class="app__content-lessons">
			<Lessons {lessons} />
		</div>
	</div>
</div>

<style scoped>
	.app {
		gap: 5px;
		display: flex;
		flex-direction: column;
	}

	.app__header,
	.app__content {
		padding: 5px;
	}

	.app__header {
		font-weight: bold;
		text-align: center;
		background-color: pink;
		text-transform: uppercase;
	}

	.app__content {
		gap: 5px;
		display: flex;
		flex-direction: column;
	}
	.app__content-swars {
		top: 0;
		position: sticky;
	}
</style>
