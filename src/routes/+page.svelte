<script>
	import Footer from '$lib/Footer.svelte';
	import MintToken from '$lib/MintToken.svelte';
	import Navbar from '$lib/Navbar.svelte';
</script>

<div class="h-full w-full flex flex-col items-center" style="height:100vh;">
	<Navbar></Navbar>
	<div class="h-full w-full flex flex-col items-center justify-center">
		<div class="mb-6" style="font-size:40px;margin-top:-10vh;">
			<div>Gluon-Based Gold</div>
			<div>Stablecoins on Ergo</div>
		</div>
		<MintToken></MintToken>
	</div>
</div>
<Footer></Footer>
