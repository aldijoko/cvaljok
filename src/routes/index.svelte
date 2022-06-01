<script context="module">
	export const prerender = true;
</script>

<script>
	import Counter from '$lib/Counter.svelte';
	import Component from '$lib/components/home/index.svelte'
</script>

<svelte:head>
	<title>CV Aldi Joko</title>
	<meta name="description" content="Portofolio Aldi Joko" />
</svelte:head>

<section>

	<Component/>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	/* h1 {
		width: 100%;
	} */

	/* .welcome {
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	} */
</style>
