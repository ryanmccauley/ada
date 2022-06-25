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
		<div class="flex flex-col gap-2">
			<h4 class="font-bold text-2xl underline underline-offset-4 font-serif">Mission Statement</h4>
			<p>Lorem isplum blah blah</p>
		</div>
	</div>
</div>