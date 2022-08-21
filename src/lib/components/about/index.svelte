<script>
</script>

<div class="w-full">
	<div class="bg-img" />
	<div class="w-full bg-gray-300">
		<div class="base-container pt-40">
			<div class="w-full relative">
				<div class="top-left"></div>
				<div class="top-right"></div>
				<div class="bottom-left"></div>
				<div class="bottom-right"></div>
				<div class="w-1/2 h-[300px] bg-white border border-gray-600 rounded-md shadow-md absolute -top-44 left-1/2 transform -translate-x-1/2 -translate-y-1/2 flex">
					<div class="w-1/2 h-full">
						<img class="w-full h-full object-contain" src="/profilefoto.JPG" alt="">
					</div>
					<div class="w-full h-full">
						<div class="w-full p-5">
							<div class="w-full my-1 text-center">
								<h1 class="text-xl font-semibold mb-2">Muhammad Aldi Joko Satria Perdana</h1>
								<p class="text-lg text-gray-400">Frontend Developer</p>
							</div>
							<div class="w-full flex my-8">
								<div class="w-full">
									<p>Email:</p>
									<p>Phone:</p>
								</div>
								<div class="w-full font-semibold">
									<p>maldijokosp@gmail.com</p>
									<p>08981187320</p>
								</div>
							</div>
							<div class="w-full flex my-5">
								<div class="w-full ">
									<p>Date of Birth:</p>
									<p>Location:</p>
								</div>
								<div class="w-full font-semibold">
									<p>22 September 1997</p>
									<p>Yogyakarta, Indonesia</p>
								</div>
							</div>
							
						</div>
					</div>
				</div>
			</div>
			<div class="w-full pt-14 text-center">
				<h1 class="text-4xl font-bold">Work Experience</h1>
				<div class="w-full p-5">
					
				</div>
			</div>
			
		</div>
	</div>
</div>

<style>
	.bg-img {
		background-image: linear-gradient(359.68deg, #222b65 0.29%, rgba(34, 43, 101, 0.4) 99.73%),
			url('/bgView.jpg');
		background-position: center;
		background-repeat: no-repeat;
		background-size: cover;
		width: 100%;
		height: 420px;
	}

	.top-left, .top-right, .bottom-left, .bottom-right {
		position: absolute;
		height: 50px;
		width: 100px;
		background: #e6e6e6;
		box-shadow: 0px 3px 15px rgba(0,0,0,0.2);
		z-index: 1;
	}

	.top-left {
		top: -345px;
		left: 250px;
		transform: rotate(-45deg);
	}

	.top-right {
		top: -345px;
		right: 250px;
		transform: rotate(45deg);
	}

	.bottom-left {
		top: -60px;
		left: 250px;
		transform: rotate(45deg);
	}

	.bottom-right {
		top: -60px;
		right: 250px;
		transform: rotate(-45deg);
	}
</style>
