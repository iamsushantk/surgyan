<script>
	import lessons from '../data/lessons';

	import Swars from './Swars.svelte';
	import Lessons from './Lessons.svelte';
</script>

<div class="app">
	<div class="content">
		<div class="swars">
			<Swars />
		</div>
		<div class="lessons">
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

	.app > .content {
		display: flex;
		gap: var(--space-xx);
		flex-direction: column;
		padding: var(--space-xx);
	}

	.app > .content > .swars {
		top: 0;
		position: sticky;
	}
</style>
