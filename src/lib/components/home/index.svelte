<script>
	import { slide } from 'svelte/transition';
	import { fly, fade } from 'svelte/transition';
	import { goto } from '$app/navigation';

	const onClick = () => {
		alert('Terimakasih, Ditunggu informasi selanjutnya')
	}

</script>

<div class="w-full pt-24 h-full bg-blue-300">
	<div class="base-container flex p-7 ">
		<img src="/hello.svg" alt="avatar" class="w-1/2 hidden md:flex"  transition:slide="{{duration: 200}}"/>
		<div class="p-14 px-20">
			<p class="font-serif text-3xl font-normal italic tracking-widest mb-5">Hello!</p>
			<p class="text-5xl font-semibold mb-10">I'm Aldi Joko</p>
			<p class="text-3xl font-mono tracking-wide underline-offset-8 mb-3">
				<a class="underline decoration-red-500">Jr. Frontend Developer</a>
			</p>
			<div class="w-full flex gap-3 items-center justify-center mb-8">
				<p class="w-full italic text-sm">Check Out My :</p>
				<ul class="w-full flex gap-3">
					<li class="circle flex items-center justify-center">
						<a href=""><span class="iconify icon" data-icon="akar-icons:twitter-fill"></span></a>
					</li>
					<li class="circle flex items-center justify-center">
						<a href=""><span class="iconify icon" data-icon="akar-icons:instagram-fill"></span></a>
					</li>
					<li class="circle flex items-center justify-center">
						<a href="https://www.linkedin.com/in/muhammad-aldi-joko-satria-perdana-3b955a13b"><span class="iconify icon" data-icon="akar-icons:linkedin-box-fill"></span></a>
					</li>
					<li class="circle flex items-center justify-center">
						<a href="https://github.com/aldijoko"><span class="iconify icon" data-icon="akar-icons:github-fill"></span></a>
					</li>
				</ul>
			</div>
			<div class="w-full" >
				<div class="mb-5">
					<a href="" on:click={onClick} download class="btn w-full" in:fly="{{ x: 200 }}" out:fade>Download CV ATS</a>
					<p class="text-xs text-red-500 font-bold">*Last updated June 2022</p>
				</div>
				<div>
					<a href="" download class="btn w-full" on:click={onClick} in:fly="{{ y: 200 }}" out:fade>Download CV Creative</a>
					<p class="text-xs text-red-500 font-bold">*Last updated March 2022</p>
				</div>
				
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
		@apply flex items-center justify-center font-medium not-italic px-8 py-2 rounded-md text-center bg-red-500 text-white;
	}

	.btn:hover {
		background-color: white;
		color: red;
	}
</style>
