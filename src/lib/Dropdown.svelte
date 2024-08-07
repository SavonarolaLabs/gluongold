<script lang="ts">
	let menuOpen = false;
	let hoverTimeout: number;

	function handleMouseEnter() {
		clearTimeout(hoverTimeout);
		menuOpen = true;
		setZIndexTo10();
	}

	function handleMouseLeave() {
		hoverTimeout = window.setTimeout(() => {
			menuOpen = false;
		}, 200); // Adjust the delay as needed
	}

	let element: HTMLElement;

	function setZIndexTo10() {
		const elements = document.querySelectorAll('.zfix');
		elements.forEach((el) => {
			(el as HTMLElement).style.zIndex = '10';
		});
		if (element) {
			element.style.zIndex = '11';
		}
	}
</script>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<div class="absolute" style="right:10px; top:13px;">
	<div
		bind:this={element}
		class="zfix relative inline-block text-left"
		on:mouseenter={handleMouseEnter}
		on:mouseleave={handleMouseLeave}
	>
		<div>
			<button class="flex items-center btn_active"
				><span class="mr-2 pl-2">ERG</span>
				<svg width="12" height="7" viewBox="0 0 12 7" fill="none" xmlns="http://www.w3.org/2000/svg"
					><path d="M0.97168 1L6.20532 6L11.439 1" stroke="black" stroke-width="1.5"></path></svg
				></button
			>
		</div>

		<div
			class={`dropdown btn_active  ${menuOpen ? 'show' : ''}`}
			role="menu"
			aria-orientation="vertical"
			aria-labelledby="menu-button"
			tabindex="-1"
			style="display: ${menuOpen ? 'block' : 'none'};"
		>
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<div class="balance text-sm">
				<div class="flex items-center text-lg">Buy Gold</div>
				<div class="balance-total">ERG &#8594; GAU + GAUC</div>
			</div>
			<div class="balance text-sm">
				<div class="flex items-center text-lg">Sell Gold</div>
				<div class="balance-total">GAU + GAUC &#8594; ERG</div>
			</div>
			<div class="balance text-sm">
				<div class="flex items-center text-lg">Gold to Yield</div>
				<div class="balance-total">GAU &#8594; GAUC</div>
			</div>
			<div class="balance text-sm">
				<div class="flex items-center text-lg">Yield to Gold</div>
				<div class="balance-total">GAUC &#8594; GAU</div>
			</div>
		</div>
	</div>
</div>

<style>
	.balance {
		margin-bottom: 0.5rem;
		padding: 1em;
		background-color: var(--fill-container);
		color: var(--text-secondary);
	}

	.balance-total {
		color: var(--cl-light-gray);
		display: flex;
		justify-content: space-between;
	}

	.actions {
		display: flex;
		gap: 0.5rem;
		margin-bottom: 1rem;
	}

	.actions button {
		flex: 1;
		padding: 0.5rem;
		border: none;
		border-radius: 0.25rem;
		transition: background-color 0.2s;
	}

	.actions button.deposit {
		background-color: #3b82f6; /* Blue color */
		color: white;
	}

	.actions button.withdraw {
		background-color: #1f2937;
		color: white;
	}

	.actions button.deposit:hover {
		background-color: #2563eb;
	}

	.actions button.withdraw:hover {
		background-color: #374151;
	}

	.dropdown {
		display: none;
		position: absolute;
		left: 0;
		top: 100%;
		z-index: 1000;
		width: max-content;
		min-width: 12rem;
		margin: 0.25rem 0 0;
		font-size: 0.875rem;
		color: #212529;
		text-align: left;
		list-style: none;
		background-color: #fff;
		background-clip: padding-box;
	}

	.dropdown.show {
		display: block;
	}
</style>
