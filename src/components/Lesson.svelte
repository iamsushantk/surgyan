<script>
	export let lesson;
	import Alankar from './Alankar.svelte';
</script>

<div class="flex gap-2 border-solid border-0 border-indigo-800 flex-col">
	<div class="p-4 font-bold text-center bg-indigo-800 text-white">{lesson.name}</div>
	{#each lesson.alankars as alankar}
		<Alankar {alankar} />
	{/each}
</div>
