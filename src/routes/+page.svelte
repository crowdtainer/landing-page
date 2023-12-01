<script lang="ts">
	import { onMount } from 'svelte';
	import { typewriter } from '$lib/transitions.js';

	var messages = new Array(
		['Invite friends to support your project.'],
		['Build your dreams.'],
		['Fund your book.'],
		['Buy in group to get discounts.'],
		['Kickstart your side-project.'],
		['What will you build, anon?']
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

<div class="flex justify-center sm:pt-10 mt-5">
	<img class="lg:h-36 md:h-32 h-28" alt="Crowdtainer Logo" src="images/CrowdtainerLogo.svg" />
</div>
<div class="flex justify-center sm:pt-10">
	<div
		class="bg-gradient-to-r from-blue-600 via-green-500 to-indigo-400 inline-block text-transparent bg-clip-text"
	>
		<div class="font-extrabold text-2xl">Crowdtainer</div>
	</div>
</div>
<div class="flex justify-center text-3xl mx-w-2xl">
	<p class="mt-8 mx-8 text-center">
		Fund and scale your ideas & projects today using open source software.
	</p>
</div>

<div class="flex justify-center my-8 pt-8">
	<div class="text-black dark:text-gray-100 mx-10">
		<div class="mockup-code bg-gray-900 shadow-2xl">
			{#key index}
				<pre data-prefix=">">
					<code
						class=" -ml-44 text-xs md:text-sm lg:text-xl text-green-500"
						in:typewriter|global={{ speed: 3 }}>{`${messages[index]}` || ''}</code
					>
			</pre>
			{/key}
		</div>
	</div>
</div>

<div class="flex justify-center my-16">
	<div class="mx-10 space-y-5 text-center">
		<div class="sm:flex items-center w-auto">
			<div class="">
				<div class="pb-4 text-3xl">Features:</div>

				<ul class="list-none text-left list-outside hover:list-inside md:text-xl text-md">
					<li>⚡️ <b>ERC-20</b> support for payment.</li>
					<li>⚡️ Participation proof as <b>ERC-721</b>.</li>
					<li>⚡️ WalletConnect v1 & injected wallet support.</li>
					<li>⚡️ Batteries included (optional modules):</li>
					<li class="ml-4">⚡️ <b>On-chain referrals.</b></li>
					<li class="ml-4">⚡️ <b>WooCommerce</b> integration for invoice/accounting.</li>
					<li class="ml-4">⚡️ Off-chain join authorization (Signature-based).</li>
					<li class="ml-4">⚡️ Self-hosted anti-sybil / SPAM prevention.</li>
				</ul>
			</div>
		</div>
	</div>
</div>

<div class="flex justify-center my-5 mb-10 space-x-2 mx-2">
	<a href="https://github.com/crowdtainer/dapp-contracts" target="_blank" rel="noreferrer"
		><div class="btn active-btn">Smart contract 🔗</div>
	</a>
	<a href="https://github.com/crowdtainer/dapp-web" target="_blank" rel="noreferrer">
		<div class="btn active-btn">Frontend / Backend 🔗</div>
	</a>
</div>

<div class="flex justify-center items-center my-16 mx-4 mb-18">
	<div class="flex flex-wrap items-center">
		<div class="space-y-5 text-center">
			<div class="bg-gray-100 dark:bg-gray-800 p-8 rounded-xl">
				<div class="px-2">
					<!-- </span> -->
					<div class="inline-block pb-4 text-xl">
						Example application:
						<div class="link"><a href="https://app.barterfly.de">Group Buying</a></div>
					</div>
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
	</div>
</div>

<div class="mb-20">
	<div class="flex justify-center text-3xl">
		<p class="mt-8 mx-8 text-center max-w-xl">
			Self-hosting & standing by the original web3 principles.
		</p>
	</div>
</div>

<div class="flex justify-center my-10">
	<div class="mx-10 space-y-5 max-w-3xl">
		<div class="sm:flex items-center">
			<div class="text-xl">
				While others are attempting to rewrite the definition of web3, Crowdtainer cuts no corners
				whenever possible.
			</div>
		</div>
	</div>
</div>

<div class="flex justify-center my-10">
	<div class="mx-10 space-y-5 max-w-3xl">
		<div class="sm:flex items-center">
			<div class="text-xl">
				With Crowdtainer, you can eliminate the necessity for multiple intermediary companies when
				funding a project: minimize compounding fees and the involvement of several entities in
				agreements between two parties (service/product provider and supporters).
			</div>
		</div>
	</div>
</div>

<div class="flex justify-center my-10">
	<div class="mx-10 space-y-5 max-w-3xl">
		<div class="sm:flex items-center">
			<div class="text-xl">
				Streamline the functions typically handled by crowdfunding companies and multiple payment
				intermediaries, thereby reducing the accumulation of charges and data sharing.
			</div>
		</div>
	</div>
</div>

<section class="py-2 mx-4 mb-4 flex justify-center w-full sm:w-auto">
	<div class=" max-w-3xl text-center drop-shadow-2xl rounded-[15px] py-2 md:p-4">
		<h2 class="text-2xl lg:text-3xl font-bold p-8">Crowdtainer community</h2>
		<a href="https://discord.gg/D6FrwCfKAP" target="_blank" rel="noreferrer">
			<div class="flex justify-center">
				<img
					src="/images/groupChat.png"
					class="justify-center align-center w-6 lg:w-auto h-20"
					alt="github"
				/>
			</div>
			<div class="flex justify-center">
				<button
					class="mx-2 items-center bg-green-800 hover:bg-green-600 min-w-max gap-2 lg:gap-4 btn active-btn mt-4 flex text-gray-200 py-2 outline-none focus:outline-none mb-1 ease-linear transition-all duration-150"
					type="button"
				>
					<div class="text-sm lg:text-xl font-semibold h-full">Discord / Chat</div>
				</button>
			</div>
		</a>
	</div>
</section>

<div class="mb-16">
	<div class="flex justify-center text-xl">
		<p class="mt-2 mx-8 text-center max-w-xl">
			While we're <a href="https://app.barterfly.de" class="link">dogfooding</a> this project, there's
			a lot more that needs to be done. Join our discord channel and participate on this journey.
		</p>
	</div>
</div>

<div class="mb-20">
	<div class="flex justify-center text-3xl">
		<p class="mt-4 mx-8 text-center max-w-xl">
			Let's bring unique projects, products, and ideas to life.
		</p>
	</div>
</div>
