<script lang="ts">
	import { Swiper, SwiperSlide } from 'swiper/svelte';
	import { EffectCards } from "swiper";
	import 'swiper/css';
	import "swiper/css/effect-cards";

	let testSlides = [];
	for (let i = 0; i < 10; i++) {
		testSlides.push(i);
	}
</script>

<div class="flex space-between py-8">
	<div class="flex flex-col w-full gap-12">
		<!--<div>
			<Swiper
				effect={"cards"}
				grabCursor={true}
				modules={[EffectCards]}
				on:slideChange={() => console.log('slide change')}
				on:swiper={(e) => console.log(e.detail[0])}
			>
				{#each testSlides as slide}
					<SwiperSlide>
						<div class="w-full h-[500px] bg-red-500 text-white rounded-2xl p-4">
							Slide {slide+1}
						</div>
					</SwiperSlide>
				{/each}
			</Swiper>
		</div>-->
		<div class="flex flex-col gap-4">
			<h4 class="font-bold text-2xl underline underline-offset-4 font-serif">Mission Statement</h4>
			<p>Lorem isplum blah blah</p>
		</div>
		<div class="flex flex-col gap-4">
			<h4 class="font-bold text-2xl underline underline-offset-4 font-serif">Our Team</h4>
			<div class="grid grid-cols-3 gap-8">
				<div class="flex flex-col gap-2">
					<img src="/Cyrus.jpg" class="w-full h-[400px]" />
					<div class="flex justify-between w-full items-center">
						<h5 class="font-medium text-xl">Cyrus Nadizadeh</h5>
						<a href="mailto:cyrusnadi@gmail.com" class="text-sky-700 underline underline-offset-4">cyrusnadi@gmail.com</a>
					</div>
				</div>
				<div class="flex flex-col gap-2">
					<img src="/Shilpa.jpg" class="w-full h-[400px]" />
					<div class="flex justify-between w-full items-center">
						<h5 class="font-medium text-xl">Shilpa Shiju</h5>
						<a href="mailto:shilpamshiju@gmail.com" class="text-sky-700 underline underline-offset-4">shilpamshiju@gmail.com</a>
					</div>
				</div>
				<div class="flex flex-col gap-2">
					<img src="/Ryan.jpeg" class="w-full h-[400px]" />
					<div class="flex justify-between w-full items-center">
						<h5 class="font-medium text-xl">Ryan McCauley</h5>
						<a href="mailto:ryanmcly@gmail.com" class="text-sky-700 underline underline-offset-4">ryanmcly@gmail.com</a>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>