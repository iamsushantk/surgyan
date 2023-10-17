<script>
	import lessons from '../data/lessons';

	import Swars from './Swars.svelte';
	import Lessons from './Lessons.svelte';
</script>

<div class="app">
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
		display: flex;
		gap: var(--space-xx);
		flex-direction: column;
	}

	.app__content {
		display: flex;
		gap: var(--space-xx);
		flex-direction: column;
		padding: var(--space-xx);
	}

	.app__content-swars {
		top: 0;
		position: sticky;
	}
</style>
