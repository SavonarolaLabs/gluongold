<script>
	import Footer from '$lib/Footer.svelte';
	import MintToken from '$lib/MintToken.svelte';
	import Navbar from '$lib/Navbar.svelte';
</script>

<div class="h-full w-full flex flex-col items-center p-4" style="height:100vh;">
	<Navbar></Navbar>
	<div class="h-full w-full flex items-center justify-center bg-red">
		<MintToken></MintToken>
	</div>
</div>
<img src="hamster.png" alt="" />
<Footer></Footer>

<style>
	img {
		position: absolute;
		top: 80%;
		left: 5%;
		width: 100px;
	}
</style>
