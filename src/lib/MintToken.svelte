<script>
	let mode = 'broke';
</script>

<div class="flex flex-col items-center" style="margin-top:-50px;">
	<img src="catcoins.png" alt="" />
	<div id="minter" class="flex flex-col gap-4 border-2 rounded-xl p-5">
		<div id="swap" class="flex flex-col relative">
			<div class="group border-2 rounded-xl p-4">
				<input type="text" class="my-1 w-full px-1" value="100" style="z-index:1;" />
				<button
					class="flex items-center btn_active absolute"
					style="right:10px; top:13px; box-shadow:none"
					><span class="mr-2 pl-2">ERG</span>
					<svg
						width="12"
						height="7"
						viewBox="0 0 12 7"
						fill="none"
						xmlns="http://www.w3.org/2000/svg"
						><path d="M0.97168 1L6.20532 6L11.439 1" stroke="black" stroke-width="1.5"></path></svg
					></button
				>
			</div>
			<div
				class="group border-2 rounded-xl p-4"
				style="border-color: var(--cl-gray);z-index:2;background:white;"
			>
				<div class="flex items-center mt-2">
					<input type="text" class="w-full px-1" value="0,387007058 GAU" />
					<span class="text-slate-500">+</span>
					<input type="text" class="w-full px-1 text-end" value="0,157624107 GAUC" />
				</div>
			</div>
			<!-- Third div in the absolute middle of #swap -->
			<div class="absolute-center">
				<div class="text-slate-500 circle flex items-center justify-center">
					<svg
						style="margin-left:-1px"
						xmlns="http://www.w3.org/2000/svg"
						width="14"
						height="14"
						viewBox="0 0 24 24"
						fill="none"
						stroke="#777"
						stroke-width="3.5"
						stroke-linecap="round"
						stroke-linejoin="round"
						><line x1="12" y1="5" x2="12" y2="19"></line><polyline points="19 12 12 19 5 12"
						></polyline></svg
					>
				</div>
			</div>
		</div>
		<div class="group w-full hints p-4 flex flex-col gap-2 text-slate-800">
			<div class="ml-2">GAU is pegged to 1 gram of Gold.</div>
			<div class="ml-2">
				GAUC is volatile, it gives leveraged exposure to ERG and protocol fees.
			</div>
		</div>
		<button class="btn rounded-xl mt-5">swap</button>
	</div>
</div>

<style lang="postcss">
	.group {
		border-color: var(--cl-gray);
		box-shadow: 4px 4px 0px #333;
	}

	.hints {
		border: 2px solid #333;
		border-radius: 15px;
		background-color: var(--cl-yellow);
	}

	#minter {
		width: 400px;
		background: white;
		border-color: #333;
		border-width: 4px;
		box-shadow: 8px 8px 0px #333;
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
		border-width: 5px 2px 2px 5px; /* top right bottom left */
		border-style: solid;
		border-color: #333;
		border-radius: 50%;
		background-color: white;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 24px;
	}
</style>
