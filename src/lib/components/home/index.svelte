<script>
	import { slide } from 'svelte/transition';
	import { goto } from '$app/navigation';

	function onClick() {
		console.log('tes')
	}
</script>

<div class="w-full pt-24 h-full bg-blue-300">
	<div class="base-container flex p-7 " >
		<img src="/hello.svg" alt="avatar" class="w-1/2" />
		<div class="p-14 px-20">
			<p class="font-serif text-3xl font-normal italic tracking-widest mb-5">Hello!</p>
			<p class="text-5xl font-semibold mb-10">I'm Aldi Joko</p>
			<p class="text-3xl font-mono tracking-wide underline-offset-8 mb-3">
				<a class="underline decoration-red-500">Frontend Developer</a>
			</p>
			<div class="w-full flex gap-3 items-center justify-center mb-8">
				<p class="w-full italic text-sm">Check Out My :</p>
				<ul class="w-full flex gap-3">
					<li class="circle flex items-center justify-center">
						<a href="https://twitter.com/aldijokosp"><span class="iconify icon" data-icon="akar-icons:twitter-fill"></span></a>
					</li>
					<li class="circle flex items-center justify-center">
						<a href="https://instagram.com/aldijoko_aljok"><span class="iconify icon" data-icon="akar-icons:instagram-fill"></span></a>
					</li>
					<li class="circle flex items-center justify-center">
						<a href="https://www.linkedin.com/in/muhammad-aldi-joko-satria-perdana-3b955a13b"><span class="iconify icon" data-icon="akar-icons:linkedin-box-fill"></span></a>
					</li>
					<li class="circle flex items-center justify-center">
						<a href="https://github.com/aldijoko"><span class="iconify icon" data-icon="akar-icons:github-fill"></span></a>
					</li>
				</ul>
			</div>
			<div class="w-full">
				<button class="btn w-full mb-5" on:click={() => goto('/about')}>About Me!</button>
				<button class="btn w-full">Download CV</button>
			</div>
		</div>
		<!-- <div>
			tes
		</div> -->
	</div>
	<div>
		
	</div>
</div>

<style lang="postcss">
	.circle {
		height: 30px;
		width: 30px;
		background-color: #bbb;
		border-radius: 50%;
	}

	.icon:hover {
		color: #1DA1F2;
	}

	.btn {
		@apply flex items-center justify-center font-medium not-italic px-8 py-2 rounded-md bg-red-500 text-white;
	}

	.btn:hover {
		background-color: white;
		color: red;
	}
</style>
