<script>
	export let lesson;
	import Alankars from './Alankars.svelte';
</script>

<div class="lesson">
	<div class="header">{lesson.name}</div>
	<Alankars alankars={lesson.alankars} />
</div>

<style scoped>
	.lesson {
		display: flex;
		gap: var(--space-xx);
		flex-direction: column;
	}

	.lesson > .header {
		font-weight: bold;
		text-align: center;
		padding: var(--space-xx);
		background-color: pink;
		border-top-left-radius: 20px;
		border-top-right-radius: 20px;
	}
</style>
