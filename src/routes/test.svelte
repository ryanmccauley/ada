<script lang="ts">
	import { Swiper, SwiperSlide } from 'swiper/svelte';
	import { Pagination } from "swiper";
	import 'swiper/css';
	import "swiper/css/pagination";

	let slides = [];
	for (let i = 0; i < 5; i++) {
		slides.push(i);
	}
</script>

<Swiper
	pagination={{
				dynamicBullets: true,
			}}
	modules={[Pagination]}
	on:slideChange={() => console.log('slide change')}
	on:swiper={(e) => console.log(e.detail[0])}
>
	{#each slides as slide}
		<SwiperSlide>
			<div class="min-h-[400px] min-w-[400px] border">
				Slide {slide+1}
			</div>
		</SwiperSlide>
	{/each}
</Swiper>