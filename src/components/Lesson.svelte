<script>
	import Alankar from './Alankar.svelte';

	export let lesson;
</script>

<div class="accordion accordion-flush">
	<div class="bg-primary text-white text-center p-2 my-2 rounded">{lesson.name}</div>
	<div class="d-flex flex-column gap-2">
		{#each lesson.alankars as alankar (alankar.id)}
			<div class="accordion-item">
				<h2 class="accordion-header">
					<button
						class="accordion-button collapsed"
						type="button"
						data-bs-toggle="collapse"
						data-bs-target={`#alankar-${alankar.id}`}
					>
						Lesson #{alankar.id}
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
</div>
