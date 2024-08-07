<script lang="ts">
	import Kitty from './Kitty.svelte';
</script>

<div
	class="bg-white pt-2 px-6 font-normal w-full flex justify-between items-center"
	style="
	 background: rgba(255, 255, 255, 0.3);
    backdrop-filter: blur(10px);
	min-height:100px; 
	border-bottom:1px solid var(--cl-light-gray);
	"
>
	<div class="text-2xl flex items-center brand-font" style="font-size:40px">
		<Kitty></Kitty>
		<div class="mb-1 ml-2 font-thin" style="font-family: 'Open Sans';">Gluon Gold</div>
	</div>

	<div class="flex items-center gap-6">
		<div
			class="btn_active"
			style="
			border: none;
		background-color:rgba(255,255,255,0.5);
		"
		>
			Swap
		</div>
		<div>FAQ</div>
	</div>

	<div
		class="btn_active mr-2"
		style="
			border: none;
		background-color:rgba(255,255,255,0.7);
		"
	>
		Connect
	</div>
</div>
