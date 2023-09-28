<script lang="ts">
	import { onMount } from 'svelte';
	import { typewriter } from '$lib/transitions.js';

	var messages = new Array(
		['Invite friends to support your project.'],
		['Build your dreams.'],
		['Fund your book.'],
		['Buy in group & get discounts.'],
		['Kickstart that side-project.'],
		['What will you build, anon?'],
	);
	let index = 0;

	onMount(() => {
		const interval = setInterval(() => {
			index += 1;
			index %= messages.length;
		}, 4500);

		return () => {
			clearInterval(interval);
		};
	});
</script>

<div class="flex justify-center my-16 pt-16">
	<div class="text-black dark:text-gray-100 mx-10">
		<div class="mockup-code bg-gray-900 shadow-2xl">
			{#key index}
				<pre data-prefix=">">
					<code class=" -ml-44 text-sm md:text-md lg:text-xl text-green-500" in:typewriter={{ speed: 3 }}
						>{`${messages[index]}` || ''}</code
					>
			</pre>
			{/key}
		</div>
	</div>
</div>
<div class="flex justify-center text-3xl mx-w-2xl">
	<p class="mt-8 mx-8 text-center">
		Fund, operate, and scale your ideas & communities transparently on Ethereum.
	</p>
</div>

<div class="container mx-auto flex justify-center items-center my-10">
	<div class="flex flex-wrap items-center">
		<div class="pl-0 sm:pl-10 lg:pl-40 space-y-5 text-center md:shrink-0 ">
			<div class="flex justify-center sm:py-10">
				<img class="lg:h-36 md:h-32 h-28" alt="Crowdtainer Logo" src="images/CrowdtainerLogo.svg" />
			</div>
			<div class="">
				<div class="px-8">
					<div
						class="bg-gradient-to-r from-blue-600 via-green-500 to-indigo-400 inline-block text-transparent bg-clip-text"
					>
						<div class="font-extrabold text-2xl">Your open source group buying application.</div>
					</div>
					<!-- </span> -->

					<div class="flex justify-center mt-6">
						<ul class="text-lg list-unordered space-y-1">
							<li>
								<div
									class="bg-gradient-to-r from-blue-400 to-blue-700 inline-block text-transparent bg-clip-text"
								>
									• Merchants:
								</div>
								Sell in bulk, save in production.
							</li>
							<li>
								<h4>
									<div
										class="bg-gradient-to-r from-green-500 to-green-700 inline-block text-transparent bg-clip-text"
									>
										• Everyone:
									</div>
									Buy together, get better deals.
								</h4>
							</li>
						</ul>
					</div>
				</div>
			</div>
		</div>

		<div
			class="mx-10 sm:pl-10 md:pl-20 space-y-5 text-center shrink-0 md:my-5 sm:my-10 lg:pl-20 xl:my-36"
		>
			<div class="sm:flex items-center w-auto">
				<div class="pt-8">
					<div class="pb-4 text-xl">Features:</div>

					<ul class="list-none text-left list-outside hover:list-inside">
						<li>⚡️ <b>ERC-20</b> support for payment.</li>
						<li>⚡️ Participation proof as <b>ERC-721</b>.</li>
						<li>⚡️ <b>WalletConnect</b> support.</li>
						<li>⚡️ <b>WooCommerce</b> integration (optional).</li>
						<li>⚡️ <b>Referrals</b> (optional).</li>
						<li>⚡️ <b>Signature-based</b> Off-chain authorization.</li>
					</ul>
				</div>
			</div>
		</div>
	</div>
</div>

<div class="flex justify-center my-5 pb-20 space-x-4">
	<a href="https://github.com/crowdtainer/dapp-web" target="_blank" rel="noreferrer"
		><div class="btn active-btn">Smart contract 🔗</div>
	</a>
	<a href="https://github.com/crowdtainer/dapp-contracts" target="_blank" rel="noreferrer">
		<div class="btn active-btn">Frontend / Backend🔗</div>
	</a>
</div>

<div class="mb-40">
	<div class="flex justify-center text-3xl ">
		<p class="mt-8 mx-8 text-center max-w-xl ">
			Let's bring unique projects, products, and ideas to life.
		</p>
	</div>
</div>
