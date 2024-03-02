<script>
	import { fade } from 'svelte/transition';
</script>
<main transitionIn={fade} transitionInParams={{ duration: 200 }} transitions={true} class="p-2 justify-center text-center items-center flex h-screen">
	<div class="card bg-yellow w-full xl:w-1/2">
		<header class="">
			<img class="m-auto translate-x-3 xl:translate-x-8" width="500" src="/img/logo.png" alt="">
		</header>
		<section class="bg-light-yellow">
			<div class="overflow-hidden bg-no-repeat sm:h-60 md:h-72">
			<img src="/img/bg.jpg" alt="Rin & Len" class="sm:object-cover sm:-translate-y-10 xl:-translate-y-8 w-full">
			</div>
			<div class="p-4 text-3xl">
				<strong>
				Chào mừng "Người Nghiện" <br> đã ghé thăm
				</strong>
			</div>
		</section>
		<footer class="p-2">
			<p >Cảm ơn mọi người đã tin tưởng và lựa chọn tiệm "Người Nghiện" ạ 😭!</p> <br>
			<span class="text-xl xl:text-2xl">Made by <a class="text-secondary-300" href="https://jinpots.top">JinPots</a></span>
		</footer>
	</div>
</main>



