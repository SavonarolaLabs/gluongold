<script lang="ts">
	import Kitty from './Kitty.svelte';
</script>

<div
	class="bg-whitept-2 px-6 font-normal w-full flex justify-between items-center"
	style="min-height:100px; border-bottom:2px solid var(--cl-light-gray);"
>
	<div class="text-2xl flex items-center brand-font" style="font-size:40px">
		<Kitty></Kitty>
		<div class="mb-1 ml-2 font-thin" style="font-family: 'Open Sans';">Gluon Gold</div>
	</div>

	<div class="flex items-center gap-6">
		<div class="btn_active">Swap</div>
		<div>FAQ</div>
	</div>

	<div class="btn_active mr-2">Connect</div>
</div>
