<script lang="ts">
	import '../app.css';
	import TopMenuNav from '$lib/TopMenuNav.svelte';
	import FooterNav from '$lib/FooterNav.svelte';
</script>

<!-- bg-gray-800 dark:bg-[#0D1116] -->
<div class="flex flex-col h-screen">
	<TopMenuNav />
	<main class="flex-grow ">
		<slot />
	</main>
	<FooterNav />
</div>

<style lang="postcss">
	:global(body) {
		font-family: 'Red Hat Display', sans-serif;
	}
</style>
