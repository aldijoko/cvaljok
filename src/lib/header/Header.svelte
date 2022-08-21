<script>
	import { page } from '$app/stores';
	// import logo from './svelte-logo.svg';
	import { fade, slide } from 'svelte/transition';
	let isOpen = false;
</script>

<header class="w-screen flex items-center bg-blue-600 fixed h-16">
	<nav class="base-container flex justify-between">
		<div class="flex text-4xl gap-2">
			<a rel="prefetch" href="/" class="font-bold text-white"> Aldi </a>
			<a rel="prefetch" href="/" class="font-sans font-bold text-red-600"> Joko </a>
		</div>
		<div class="hidden md:flex justify-end header-list">
			<ul>
				<li class:is-active={$page.url.pathname === '/'}>
					<a sveltekit:prefetch href="/">Home</a>
				</li>
				<li class:is-active={$page.url.pathname === '/about'}>
					<a sveltekit:prefetch href="/about">About</a>
				</li>
				<li class:is-active={$page.url.pathname === '/portopolio'}>
					<a sveltekit:prefetch href="/portopolio">Portopolio</a>
				</li>
				<!-- <li class:is-active={$page.url.pathname === '/todos'}>
					<a sveltekit:prefetch href="/todos">Todos</a>
				</li> -->
			</ul>
		</div>
		<div class="flex md:hidden justify-end relative" on:click={() => (isOpen = !isOpen)}>
			<span class="iconify text-3xl text-white" data-icon="ci:menu-alt-02" />
		</div>

		{#if isOpen}
			<div class="absolute h-auto bg-white z-10 p-5 flex flex-col top-16 right-0 rounded-lg" transition:slide|local>
				<div 
					class="flex items-center gap-2 mb-2"
					class:isActiveMobile={$page.url.pathname === '/'}>
					<span class="iconify" data-icon="ant-design:home-outlined" />
					<a href="/">Home</a>
				</div>
				<div 
					class="flex items-center gap-2 mb-2"
					class:isActiveMobile={$page.url.pathname === '/about'}>
					<span class="iconify" data-icon="ant-design:info-outlined"></span>
					<a href="/about">About</a>
				</div>
				<div 
					class="flex items-center gap-2 mb-2"
					class:isActiveMobile={$page.url.pathname === '/portopolio'}>
					<span class="iconify" data-icon="uil:schedule"></span>
					<a href="/portopolio">Portopolio</a>
				</div>

				
			</div>
		{/if}
	</nav>
</header>

<style>
	path {
		fill: var(--background);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	.isActiveMobile {
		font-weight: bolder;
		color: blue;
	}
	.is-active {
		background-color: blue;
		color: white;
		border-radius: 25%;
	}

	.header-list a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1em;
		/* color: var(--heading-color); */
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}
	li:hover {
		background-color: blue;
		color: white;
		border-radius: 25%;
	}
</style>
