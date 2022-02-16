<script>
	let mobileNav = { isOpen: false };

	function toggle() {
		mobileNav.isOpen = !mobileNav.isOpen;
	}
</script>

<nav class="flex justify-between p-8">

	<span class="text-2xl">MyFirstApp</span>

	<div class="hidden justify-end md:block">
		<span class="text-xl p-4">Home</span>
		<span class="text-xl p-4">Link 1</span>
		<span class="text-xl p-4">Link 2</span>
	</div>

	<div class="flex md:hidden" on:click={toggle}>
		<button type="button" class="text-black hover:text-gray-600 focus:outline-none focus:text-gray-600" aria-label="toggle menu">
			<svg viewBox="0 0 20 20" class="w-6 h-6 fill-current">
				<path fill-rule="evenodd" d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"></path>
			</svg>
		</button>
	</div>


</nav>
{#if mobileNav.isOpen}
<div class="flex flex-col lg:hidden text-right pr-8">
	<span class="text-xl pb-4">Home</span>
	<span class="text-xl pb-4">Link 1</span>
	<span class="text-xl pb-4">Link 2</span>
</div>
{/if}