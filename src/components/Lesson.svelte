<script>
	export let lesson;
	import Alankar from './Alankar.svelte';
</script>

<div class="flex gap-1 flex-col">
	<div class="p-4 font-bold text-center bg-indigo-800 text-white">{lesson.name}</div>
	{#each lesson.alankars as alankar}
		<Alankar {alankar} />
	{/each}
</div>
