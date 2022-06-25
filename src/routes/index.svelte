<script lang="ts">
	import { Swiper, SwiperSlide } from 'swiper/svelte';
	import { EffectCards } from "swiper";
	import 'swiper/css';
	import "swiper/css/effect-cards";
	import Modal from '../components/Modal.svelte';

	let testSlides = [];
	for (let i = 0; i < 4; i++) {
		testSlides.push(i);
	}

	let donateDialogOpen = false;
</script>

<div class="flex space-between py-8">
	<div class="flex flex-col w-full gap-12">
		<div>
			<Swiper
				effect={"cards"}
				grabCursor={true}
				modules={[EffectCards]}
				on:slideChange={() => console.log('slide change')}
				on:swiper={(e) => console.log(e.detail[0])}
			>
				{#each testSlides as slide}
					<SwiperSlide>
						<div class="w-full h-[750px] bg-sky-900 opacity-50 text-white rounded-2xl p-4">
							Picture {slide+1}
						</div>
					</SwiperSlide>
				{/each}
			</Swiper>
		</div>
		<Modal title="Donate" bind:open={donateDialogOpen}>
			Donate today!
		</Modal>
		<div class="flex flex-col gap-2">
			<h4 class="font-bold text-2xl font-serif">Mission Statement</h4>
			<p>With over 5 million people in the US diagnosed with Alzheimer's disease today, our goal is to spread awareness and information about the nature of the disease and how to take care of loved ones affected by it.</p>
			<p class="italic">All of our donations go directly to Alzheimer and Dementia facilities, such as Azalea Gardens Memory Care, to better the environment in which the patients live.</p>
		</div>
		<div class="flex flex-col gap-4">
			<h4 class="font-bold text-2xl underline underline-offset-4 font-serif">What is Alzheimer's?</h4>
			<p>Lorem isplum blah blah</p>
		</div>
		<div class="flex flex-col gap-4">
			<h4 class="font-bold text-2xl underline underline-offset-4 font-serif">What is Dementia?</h4>
			<p>Lorem isplum blah blah</p>
		</div>
		<div class="flex flex-col gap-2">
			<h4 class="font-bold text-2xl font-serif">How can you help?</h4>
			<p>The best way to slow down and help loved ones affected by Alzheimer's is to discover it as fast as possible. Some early symptoms of Alzheimer’s include:</p>
			<ul class="list-disc ml-6">
				<li>Misplacing of items and objects</li>
				<li>Difficulty completing daily tasks</li>
				<li>Poor judgement</li>
				<li>Random episodes of anger and mood swings</li>
				<li>Trouble remembering previous conversations and events</li>
				<li>Not willing to try new things</li>
				<li>Less flexible</li>
				<li>Withdrawal from social events and family</li>
				<li>Confusion about time and place</li>
				<li>Difficulty with words and stating their thoughts</li>
				<li>Repetition</li>
			</ul>
			<p>Show affection routinely and provide them with a sense of structure:</p>
			<ul class="list-disc ml-6">
				<li>Surround them with familiar objects such as a blankets or pillows</li>
				<li>Make their favorite foods</li>
				<li>Play their favorite songs around them</li>
				<li>Bring them to social events, daily walks, and more</li>
				<li>Be there for them</li>
			</ul>
			<p>The best way to slow down the speed of Alzheimer’s is to complete puzzles and other tasks that help to stimulate the brain.</p>
		</div>
		<div class="flex flex-col gap-2">
			<h4 class="font-bold text-2xl font-serif">Our Team</h4>
			<div class="grid grid-cols-1 md:grid-cols-3 justify-center gap-8">
				<div class="flex flex-col gap-2">
					<img src="/Cyrus.jpg" class="w-full max-h-[400px] sm:h-[400px]" />
					<div class="flex justify-between w-full items-center">
						<h5 class="font-medium text-lg">Cyrus Nadizadeh</h5>
						<a href="mailto:cyrusnadi@gmail.com" class="text-sky-700 underline underline-offset-4">cyrusnadi@gmail.com</a>
					</div>
				</div>
				<div class="flex flex-col gap-2">
					<img src="/Shilpa.jpg" class="w-full max-h-[400px] sm:h-[400px]" />
					<div class="flex justify-between w-full items-center">
						<h5 class="font-medium text-lg">Shilpa Shiju</h5>
						<a href="mailto:shilpamshiju@gmail.com" class="text-sky-700 underline underline-offset-4">shilpamshiju@gmail.com</a>
					</div>
				</div>
				<div class="flex flex-col gap-2">
					<img src="/Ryan.jpeg" class="w-full max-h-[400px] sm:h-[400px]" />
					<div class="flex justify-between w-full items-center">
						<h5 class="font-medium text-lg">Ryan McCauley</h5>
						<a href="mailto:ryanmcly@gmail.com" class="text-sky-700 underline underline-offset-4">ryanmcly@gmail.com</a>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>