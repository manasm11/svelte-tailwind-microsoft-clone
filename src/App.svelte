<script>
	import MicrosoftLogo from "./MicrosoftLogo.svelte";
	import SearchIcon from "./SearchIcon.svelte";
	import Hamburger from "./Hamburger.svelte";

	import c from "./constants";

	let showMobilMenu = false;
</script>

<main>
	<div class="navbar flex justify-between items-center">
		<div
			class="hamburger-search flex justify-center items-center md:order-2"
		>
			<Hamburger />
			<SearchIcon class="md:hidden" />
		</div>
		<div class="logo md:order-1">
			<MicrosoftLogo />
		</div>
		<div class="cart-account md:order-3">
			<SearchIcon class="hidden md:inline-block" />
			Cart Account
		</div>
	</div>
</main>
