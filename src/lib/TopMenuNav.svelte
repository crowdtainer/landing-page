<script lang="ts">
	import { page } from '$app/stores';
	import { fade } from 'svelte/transition';

	let mobileMenuOpen = false,
		profileMenuOpen = false;
	const flipMobileMenu = () => {
		mobileMenuOpen = !mobileMenuOpen;
	};
	const flipProfileMenu = () => {
		profileMenuOpen = !profileMenuOpen;
	};

	$: path = $page.url.pathname;

	import { onMount } from 'svelte';
	let isDarkMode: boolean;

	onMount(() => {
		isDarkMode = window.matchMedia('(prefers-color-scheme: dark)').matches;
	});
</script>

<nav class="bg-transparent ">
	<div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
		<div class="relative flex items-center justify-between h-16">
			<div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
				<!-- Mobile menu button-->
				<button
					type="button"
					on:click={flipMobileMenu}
					class="inline-flex items-center justify-center p-2 rounded-md hover:text-white hover:bg-gray-700 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
					aria-controls="mobile-menu"
					aria-expanded="false"
				>
					<span class="sr-only">Open main menu</span>
					<!-- Closed menu -->
					<svg
						class="{mobileMenuOpen ? 'hidden' : 'block'} h-6 w-6"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="2"
						stroke="currentColor"
						aria-hidden="true"
					>
						<path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
					</svg>
					<!-- Open menu -->
					<svg
						class="{mobileMenuOpen ? 'block' : 'hidden'} h-6 w-6"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="2"
						stroke="currentColor"
						aria-hidden="true"
					>
						<path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
					</svg>
				</button>
			</div>
			<div class="flex-1 flex items-center justify-center sm:items-stretch sm:justify-start">
				<div class="flex-shrink-0 flex items-center">
					{#if path != '/'}
						<a href="/">
							<img
								class="block lg:hidden h-8 w-auto"
								src="/images/CrowdtainerLogo.svg"
								alt="Workflow"
							/>
						</a>
					{/if}
					{#if isDarkMode}
						<a href="/">
							<img
								class="hidden lg:block h-8 w-auto"
								src="/images/TopNavbarLogo.svg"
								alt="Workflow"
							/>
						</a>
					{:else}
						<a href="/">
							<img
								class="hidden lg:block h-8 w-auto"
								src="/images/TopNavbarLogoDark.svg"
								alt="Workflow"
							/>
						</a>
					{/if}
				</div>
				<div class="hidden sm:block sm:ml-6">
					<div class="flex space-x-4">
						<a href="/Screenshots" class={path === '/Screenshots' ? 'active-btn' : 'inactive-btn'}
							>Screenshots</a
						>
						<a href="/About" class={path === '/About' ? 'active-btn' : 'inactive-btn'}>About</a>
					</div>
				</div>
			</div>
		</div>
	</div>

	<!-- Mobile menu, show/hide based on menu state. -->
	{#if mobileMenuOpen}
		<div transition:fade={{ duration: 200 }} class="sm:hidden" id="mobile-menu">
			<div class="px-2 pt-2 pb-3 space-y-1">
				<!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->

				<a
					href="/Screenshots"
					class={path === '/Screenshots' ? 'mobile-active-btn' : 'mobile-inactive-btn'}
					on:click={() => {
						mobileMenuOpen = false;
					}}>Screenshots</a
				>
				<a
					href="/About"
					class={path === '/About' ? 'mobile-active-btn' : 'mobile-inactive-btn'}
					on:click={() => {
						mobileMenuOpen = false;
					}}>About</a
				>
			</div>
		</div>
	{/if}
</nav>
