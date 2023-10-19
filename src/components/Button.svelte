<script>
	export let onClick;
	export let className;
</script>

<button type="button" class={className} on:click={onClick}>
	<slot />
</button>
