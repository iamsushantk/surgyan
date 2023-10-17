<script>
	export let lesson;
	import Alankars from './Alankars.svelte';
</script>

<div class="lesson">
	<div class="lesson__header">{lesson.name}</div>
	<Alankars alankars={lesson.alankars} />
</div>

<style scoped>
	.lesson {
		gap: 5px;
		display: flex;
		flex-direction: column;
	}

	.lesson__header {
		padding: 5px;
		font-weight: bold;
		text-align: center;
		background-color: pink;
		border-top-left-radius: 20px;
		border-top-right-radius: 20px;
	}
</style>
