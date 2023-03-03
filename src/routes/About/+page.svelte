<div class="flex justify-center  my-6">
	<div class="">
		<img class="my-8 h-32 w-32 rounded-full" src="/images/CrowdtainerLogo.svg" alt="" />
	</div>
</div>
<div class="flex justify-center">
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

					<!-- What -->
					<h2 class="text-primary">What?</h2>
					<p class="lead dark:text-gray-300">
						Crowdtainer is an <a href="https://github.com/crowdtainer">open source</a> group buying application.
						With Crowdtainer, groups of people with similar interests can easily discover whether there
						is enough interest in a certain product or service.
					</p>
					<p>
						It strives to be abstract enough to be used for a variety of projects, essentially any
						situation where pooling funds for a common goal is desired.
					</p>
					<p>
						When enough funds are pooled, an atomic set of bulk orders can be performed by the
						service provider. If not, participants withdraw their funds (ERC20) back.
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
								<b>A service/product provider</b>, which offers a sale contract (or other custom agreement) via the platform and
								would usually be the legal counterpart responsible for shipping the products to the
								participants (or provider the promised services). Usually this is also the party hosting the frontend.
							</p>
						</li>
					</ol>

					<!-- How -->
					<h2 class="text-primary">How?</h2>

					<p>
						I (my company) have deployed and host an "instance" of the platform (this website), and
						display only the product(s) that I sell myself as a company. Participating in any of my
						campaigns will help develop this project further. However, people are free and
						encouraged to take all the open source code and do their own deployments with their own
						projects.
					</p>
					<p>
						On the surface, the platform is similar to other crowdfunding platforms, but at a closer
						look you will see a few important differences:
					</p>
					<ul>
						<li>
							<b>Credit cards are not required.</b> Neither there is a "crowdfunding company", since
							this part is
							<b>automated by the smart contracts</b> which lives on Ethereum.
						</li>
						<li>
							<b>Improved privacy.</b> There are ways to improve the status quo when it comes to online
							orders and privacy by using zero knowledge proofs to prove participation. More details
							on this soon.
						</li>
						<li>
							<b>Custody.</b> The service/product provider does not have access to customer funds at
							all until the minimum target is reached and the bulk transfer can be completed "at once" or not at all.
							This not only makes sense in general, but avoids legal problems that would arrise if a
							company/person is (even if temporarily) managing and holding customer funds before the
							project is known to be successfull.
						</li>
					</ul>

				</div>
			</article>
		</div>
	</div>
</div>
