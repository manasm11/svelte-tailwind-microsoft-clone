<script>
	import MicrosoftLogo from "./components/MicrosoftLogo.svelte";
	import Search from "./components/Search.svelte";
	import HamburgerCross from "./components/HamburgerCross.svelte";
	import Cart from "./components/Cart.svelte";
	import Account from "./components/Account.svelte";

	import c from "./constants";

	let showMobilFeatures = false;
</script>

<main>
	<div class="navbar flex justify-between items-center">
		<div
			class="hamburger-search flex justify-center items-center md:order-2"
		>
			<HamburgerCross
				{showMobilFeatures}
				on:click={() => (showMobilFeatures = !showMobilFeatures)}
			/>
			<Search class="md:hidden" />
		</div>
		<div class="logo md:order-1">
			<MicrosoftLogo />
		</div>
		<div class="cart-account md:order-3 flex justify-between">
			<Search class="hidden md:inline-block" />
			<Cart />
			<Account />
		</div>
	</div>
	<div class="features bg-slate-200 {showMobilFeatures || 'hidden'}">
		{#each c.FEATURES as feature}
			<div class="p-4 cursor-pointer hover:bg-slate-300">{feature}</div>
			<hr class="h-0.5 w-full bg-gray-300" />
		{/each}
	</div>
</main>
