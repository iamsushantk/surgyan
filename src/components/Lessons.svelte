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
		gap: 5px;
		display: flex;
		flex-direction: column;
	}
</style>
