<script>
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
	import Footer from '$lib/Footer/Footer.svelte';

	import Icon from '@iconify/svelte';

	
</script>

<div class="w-screen overflow-hidden">
	<Header />
	<main class="overflow-y-auto w-full h-screen">
		<slot />
		<div class="h-max">
			<Footer/>
		</div>
	</main>
</div>







<!-- <footer class="bg-blue-200">
	<div class="flex items-center gap-1">
		<p>Made With</p>
		<span class="iconify text-red-500" data-icon="ant-design:heart-filled"></span>
		<p>by <a href="https://github.com/aldijoko">Aldi Joko</a></p>
	</div>
	<span class="text-gray-500">Copyright Aldi Joko © 2022. All rights reserved.</span>
</footer> -->

<style>
	
</style>
