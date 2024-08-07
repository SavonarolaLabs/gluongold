<script>
	import Dropdown from './Dropdown.svelte';

	let mode = 'broke';
</script>

<div class="flex flex-col items-center" style="">
	<!-- <img src="catcoin.png" alt="" /> -->
	<div id="minter" class="flex flex-col gap-1 rounded-xl p-2">
		<div id="swap" class="flex flex-col relative">
			<div class="input-container group rounded-xl p-4">
				<input type="text" class="font-normal text-xl w-full px-1" value="100" style="z-index:1;" />
				<Dropdown></Dropdown>
			</div>
			<div class="input-container group rounded-xl p-4 mt-1">
				<div class="flex items-center mt-2 font-normal">
					<input type="text" class="w-full px-1" value="0,387007058 GAU" />
					<span style="color:#ddd">+</span>
					<input type="text" class="w-full px-1 text-end" value="0,157624107 GAUC" />
				</div>
			</div>
			<!-- Third div in the absolute middle of #swap -->
			<div class="absolute-center">
				<div class="text-slate-500 circle flex items-center justify-center">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						width="14"
						height="14"
						viewBox="0 0 24 24"
						fill="none"
						stroke="#ddd"
						stroke-width="3.5"
						stroke-linecap="round"
						stroke-linejoin="round"
						><line x1="12" y1="5" x2="12" y2="19"></line><polyline points="19 12 12 19 5 12"
						></polyline></svg
					>
				</div>
			</div>
		</div>
		<div
			class="input-container font-normal w-full hints p-4 flex flex-col gap-2 text-slate-700"
			style="font-family: 'Open Sans', sans-serif; color: rgba(255, 255, 255, 0.9);"
		>
			<div class="ml-2">GAU is pegged to 1 gram of Gold.</div>
			<div class="ml-2">
				GAUC is volatile, it gives leveraged exposure to ERG and protocol fees.
			</div>
		</div>
		<button class="btn rounded-xl">swap</button>
	</div>
</div>

<style lang="postcss">
	input {
		background-color: transparent;
		color: rgba(255, 255, 255);
	}
	.input-container {
		background-color: #997f3e;
	}
	.hints {
		border-radius: 15px;
	}

	#minter {
		width: 400px;
		background: rgba(0, 0, 0, 0.3);
	}

	img {
		width: 250px;
		margin-bottom: -8px;
		z-index: 1;
	}

	#swap {
		position: relative; /* Ensure the child is positioned relative to this container */
	}

	.absolute-center {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		z-index: 3; /* Ensure it appears above other elements */
	}

	.circle {
		width: 42px;
		height: 42px;
		border-width: 3px; /* top right bottom left */
		border-style: solid;
		border-color: #705d2f;
		border-radius: 50%;
		background: #997f3e;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 24px;
	}
</style>
