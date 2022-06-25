<script lang="ts">
	import IoIosClose from 'svelte-icons/io/IoIosClose.svelte';
	import { fade } from 'svelte/transition';
	import { donateDialogOpen } from '../stores/donate';

	export let title: string;

	let open = $donateDialogOpen;
	donateDialogOpen.subscribe(_open => {
		open = _open;
	});
	const toggle = () => donateDialogOpen.set(!$donateDialogOpen);
</script>

{#if open}
<div class="z-50 bg-black fixed top-0 left-0 min-h-screen w-full bg-opacity-70 flex flex-col items-center justify-center" on:click={toggle}>
	<div on:click={(e) => e.stopPropagation()} transition:fade={{ duration: 100 }} class="bg-white w-4/5 max-w-xl max-h-[90%] min p-6 flex flex-col gap-2 rounded-lg">
		<div class="flex w-full justify-between items-center overflow-y-auto">
			<h5 class="font-bold text-2xl">{ title }</h5>
			<span on:click={toggle} class="h-8 w-8 hover:bg-gray-200 rounded-full cursor-pointer">
				<IoIosClose />
			</span>
		</div>
		<slot />
	</div>
</div>
{/if}