<script>
	import { page } from '$app/stores';
	import logo from './svelte-logo.svg';
</script>

<header class="w-screen flex items-center bg-blue-600 fixed h-16">

	<nav class="base-container flex justify-between">
		<div class="flex text-4xl gap-2">
			<a rel="prefetch" href="/" class="font-bold text-white">
				Aldi
			</a>
			<a rel="prefetch" href="/" class="font-sans font-bold text-red-600">
				Joko
			</a>
		</div>
		<div class="flex justify-end header-list">
			<ul>
				<li class:is-active={$page.url.pathname === '/'}><a sveltekit:prefetch href="/">Home</a></li>
				<li class:is-active={$page.url.pathname === '/about'}>
					<a sveltekit:prefetch href="/about">About</a>
				</li>
				<!-- <li class:is-active={$page.url.pathname === '/todos'}>
					<a sveltekit:prefetch href="/todos">Todos</a>
				</li> -->
			</ul>
			
		</div>
		
	</nav>

	
</header>

<style>



	/* nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	} */

	/* svg {
		width: 2em;
		height: 3em;
		display: block;
	} */

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

	/* li.active::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--accent-color);
	} */

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

	/* a:hover {
		color: var(--accent-color);
	} */

	li:hover {
		background-color: blue;
		color: white;
		border-radius: 25%;
	}
</style>
