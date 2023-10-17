<script>
	export let lessons;
	import Lesson from './Lesson.svelte';
</script>

<div class="lessons">
	{#each lessons as lesson}
		<Lesson {lesson} />
	{/each}
</div>

<style scoped>
	.lessons {
		display: flex;
		gap: var(--space-xx);
		flex-direction: column;
	}
</style>
