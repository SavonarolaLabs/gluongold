<script lang="ts">
	import Kitty from './Kitty.svelte';
</script>

<div
	class="w-full bg-yellow shadow-bot px-4 rounded-xl flex justify-between items-center"
	style="min-height:100px; border-color: #333; border-width: 4px;"
>
	<div class="text-2xl flex items-center brand-font" style="font-size:40px">
		<Kitty></Kitty>
		<div class="mb-1 ml-2" style="color:#E8C019;">Gluon Gold</div>
	</div>

	<div class="flex items-center gap-6">
		<div class="btn_active">Swap</div>
		<div>FAQ</div>
	</div>

	<div class="btn_active mr-2" style="box-shadow: 6px 6px 0 #FFDA4A;">Connect</div>
</div>
