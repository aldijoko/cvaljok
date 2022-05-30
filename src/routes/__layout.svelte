<script>
	import Header from '$lib/header/Header.svelte';
	import '../app.css';

	import Icon from '@iconify/svelte';

	
</script>

<Header />

<main>
	<slot />
</main>

<footer class="bg-blue-200">
	<div class="flex items-center gap-1">
		<p>Made With</p>
		<span class="iconify text-red-500" data-icon="ant-design:heart-filled"></span>
		<p>by <a href="https://github.com/aldijoko">Aldi Joko</a></p>
	</div>
	<span class="text-gray-500">Copyright Aldi Joko © 2022. All rights reserved.</span>
</footer>

<style>
	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		/* padding: 40px; */
	}

	footer a {
		font-weight: bold;
	}

	a:hover {
		color: aqua;
	}

	@media (min-width: 480px) {
		footer {
			padding: 10px 0;
		}
	}
</style>
