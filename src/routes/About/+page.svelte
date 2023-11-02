<div class="flex justify-center mt-10">
	<p class="font-sans text-center dark:text-gray-200 text-xl mb-2 md:mb-0 md:text-2xl">About</p>
</div>

<div class="flex flex-center">
	<div class="max-w-lg mx-auto white overflow-hidden md:max-w-7xl px-6 mb-12">
		<div class="prose lg:prose-lg prose-headings:underline prose-a:text-blue-600">
			<article
				class="prose-blockquote:font-text prose-ol:font-text prose-li:font-text prose-p:font-text prose-h2:font-display"
			>
				<div class="text-gray-900 dark:text-[#C8D1D0]">
					<!-- Why -->
					<h2 class="text-primary">Why?</h2>
					<p class="">
						<b>The boostrapping dillema:</b> Is it worth to invest "X" in project "Y"? Is there enough
						demand to justify the invesment?
					</p>
					<p>
						I was faced with this question while thinking about how to export/import coffee beans
						from my family's farm in Brazil, to Germany, whereby a minimum quantity/scale is needed
						in order for a sale to make sense in the first place.
					</p>

					<blockquote class="dark:text-[#C8D1D0]">
						Would it be possible to ship coffee abroad (from Brazil to Germany), but knowing upfront
						that there is demand, instead of sending a whole container and taking the risk that not
						enough demand is present?
					</blockquote>
					<p>
						Can we <b>crowdfund a container</b>? The journey of discovering demand is the motivation
						behind the <b>Crowdtainer</b> project.
					</p>

					<p>
						On the surface, the platform is similar to other crowdfunding platforms, but at a closer
						look you will see a few important differences:
					</p>
					<ul>
						<li>
							<b>Banks and credit cards not required.</b> Automated by the smart contracts which lives
							on Ethereum. Less fees for banks, more for your project.
						</li>
						<li>
							<b>Transparent & fair referral system.</b> Smart contracts allow the public to inspect
							the source code and make sure that friend referrals are fairly distributed.
						</li>
						<li>
							<b>Improved privacy.</b> A direct communication channel between the supplier and consumer
							reduces exposure of consumer private data: instead of multiple companies receiving data
							such as delivery details, only the actual service provider receives it. There are also
							other opportunities to improve the status quo when it comes to online orders and privacy
							by using zero knowledge proofs to prove participation.
						</li>
						<li>
							<b>Custody.</b> The service/product provider does not have access to customer funds at
							all until the minimum target is reached and the bulk transfer can be completed "at once"
							or not at all. This not only makes sense in general, but avoids legal problems that would
							arrise if a company/person is (even if temporarily) managing and holding customer funds
							before the project is known to be successfull.
						</li>
					</ul>

					<!-- What -->
					<h2 class="text-primary">What?</h2>
					<p class="lead dark:text-gray-300">
						Crowdtainer is an <a href="https://github.com/crowdtainer">open source</a> crowdfunding
						/ group buying application where groups of people with similar interests can
						discover whether there is enough interest in a certain product or service.
					</p>
					<p>
						It strives to be abstract enough to be used for a variety of projects, essentially any
						situation where pooling funds for a common goal is desired.
					</p>
					<p>
						When enough funds are pooled, the funds are withdrawn either to a service provider, a
						<a href="https://github.com/0xSplits/splits-sdk">split contract</a>, or other system to
						deliver on the promises. If the minimum goal is not reached, participants withdraw their
						funds (ERC20) back.
					</p>

					<p>An instantiation of a campaign has two main parts:</p>

					<ol>
						<li>
							<p>
								<b>The platform (infrastructure, software, tools)</b>, where people coordinate. It
								consists of Ethereum smart contracts and the interfaces to interact with the public
								ledger (where custody of money is coordinated).
							</p>
						</li>
						<li>
							<p>
								<b>A service/product provider</b>, which offers a sale contract (or other custom
								agreement) via the platform and would usually be the legal counterpart responsible
								for shipping the products to the participants (or provide the promised services).
								Usually this is also the party hosting the frontend.
							</p>
						</li>
					</ol>

					<!-- How -->
					<h2 class="text-primary">How?</h2>

					<p>
						You can see a live example 'instantiation' of Crowdtainer, hosted by Barterfly at
						<a href="https://app.barterfly.de">https://app.barterfly.de</a>, which displays only the
						offerings of Barterfly as a company. However, anyone is encouraged to take all the open
						source code and do their own deployments with their own projects (under their own
						responsability) - and of course, are welcome to contribute back with code improvements.
					</p>
					<p>
						Next steps for Crowdtainer includes improving documentation and creating tutorials, so
						that other developers and entrepreneurs can create and launch their own project easily.
					</p>
					<p>Join our discord and explore our open source repositories.</p>
				</div>
			</article>
		</div>

		<div class="py-2 mx-4 mb-8 flex justify-center w-full sm:w-auto">
			<div class=" max-w-3xl text-center drop-shadow-2xl rounded-[15px] py-2 md:p-4">
				<h2 class="text-2xl lg:text-3xl font-bold p-2">Crowdtainer community</h2>
				<a href="https://discord.gg/ZS3FcRHn" target="_blank" rel="noreferrer">
					<div class="flex justify-center">
						<img
							src="/images/groupChat.png"
							class="justify-center align-center w-6 lg:w-auto h-20 mt-8"
							alt="github"
						/>
					</div>
					<div class="flex justify-center ">
						<button
							class="mx-2 items-center bg-green-800 hover:bg-green-600 min-w-max gap-2 lg:gap-4 btn active-btn mt-4 flex text-gray-200 py-2 outline-none focus:outline-none mb-1 ease-linear transition-all duration-150"
							type="button"
						>
							<div class="text-sm lg:text-xl  font-semibold h-full">Discord / Chat</div>
						</button>
					</div>
				</a>
			</div>
		</div>
	</div>
</div>
