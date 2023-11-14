<script>
	import Alankar from './Alankar.svelte';

	export let lesson;
</script>

<div
	class="accordion accordion-flush"
	id="flushAccordion"
>
	<div class="bg-primary text-white text-center p-2 mt-2">{lesson.name}</div>
	{#each lesson.alankars as alankar (alankar.id)}
		<div class="accordion-item">
			<h2 class="accordion-header">
				<button
					class="accordion-button collapsed"
					type="button"
					data-bs-toggle="collapse"
					data-bs-target={`#alankar-${alankar.id}`}
				>
					#{alankar.id}
				</button>
			</h2>
			<div
				id={`alankar-${alankar.id}`}
				class="accordion-collapse collapse"
			>
				<div class="accordion-body">
					<Alankar {alankar} />
				</div>
			</div>
		</div>
	{/each}
</div>
