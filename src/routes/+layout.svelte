<script>
	import favicon from '$lib/assets/favicon.svg';
	import '$lib/styles/style.css'

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children()}

<img width="200px" class="corner top-left" alt="corner-thing" src="src/lib/assets/corner-thing.png">
<img width="200px" class="corner top-right" alt="corner-thing" src="src/lib/assets/corner-thing.png">
<img width="200px" class="corner bottom-left" alt="corner-thing" src="src/lib/assets/corner-thing.png">
<img width="200px" class="corner bottom-right" alt="corner-thing" src="src/lib/assets/corner-thing.png">