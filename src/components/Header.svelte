<script lang="ts">
	import { donateDialogOpen } from '../stores/donate';
	const toggle = () => donateDialogOpen.set(!$donateDialogOpen);
</script>

<header class="py-8 mx-auto max-w-7xl w-full">
	<div class="flex items-center justify-between">
		<a href="/" class="flex items-center gap-2">
			<img src="/logo.png" class="h-12" />
			<h1 class="font-bold font-serif text-3xl">Alzheimer's & Dementia Awareness</h1>
		</a>
		<div class="flex items-center gap-4">
			<button on:click={toggle} class="text-white text-xl font-medium rounded-lg px-4 bg-sky-700 hover:bg-sky-800 py-2">Donate</button>
		</div>
	</div>
</header>