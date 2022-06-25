<script lang="ts">
	import "../app.css";
	import Footer from "../components/Footer.svelte";
	import Header from "../components/Header.svelte";
</script>

<div class="flex flex-col justify-between min-h-screen mx-4">
	<Header />
	<section class="mx-auto max-w-7xl mb-auto w-full">
		<slot />
	</section>
	<Footer />
</div>
