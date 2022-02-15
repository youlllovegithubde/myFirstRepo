<script>
	let mobileNav = { isOpen: false };

	function toggle() {
		mobileNav.isOpen = !mobileNav.isOpen;
	}
</script>


<nav class="fixed bg-white shadow dark:bg-gray-800 w-full">
	<div class="container px-6 py-4 mx-auto lg:flex lg:justify-between lg:items-center">
		<div class="lg:flex lg:items-center">
			<div class="flex items-center justify-between">

				<div>
					<a class="text-2xl font-bold text-gray-800 transition-colors duration-200 transform dark:text-white lg:text-3xl hover:text-gray-700 dark:hover:text-gray-300" href="#">MyFirstApp</a>
				</div>

				<div class="flex lg:hidden" on:click={toggle}>
					<button type="button" class="text-gray-500 dark:text-gray-200 hover:text-gray-600 dark:hover:text-gray-400 focus:outline-none focus:text-gray-600 dark:focus:text-gray-400" aria-label="toggle menu">
						<svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
							<path fill-rule="evenodd" d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"></path>
						</svg>
					</button>
				</div>

			</div>

			<div class="hidden flex-col lg:flex text-gray-600 capitalize dark:text-gray-300 lg:flex lg:px-16 lg:-mx-4 lg:flex-row lg:items-center">
				<a href="#" class="mt-2 transition-colors duration-200 transform lg:mt-0 lg:mx-4 hover:text-gray-900 dark:hover:text-gray-200">features</a>
				<a href="#" class="mt-2 transition-colors duration-200 transform lg:mt-0 lg:mx-4 hover:text-gray-900 dark:hover:text-gray-200">downloads</a>
				<a href="#" class="mt-2 transition-colors duration-200 transform lg:mt-0 lg:mx-4 hover:text-gray-900 dark:hover:text-gray-200">docs</a>
				<a href="#" class="mt-2 transition-colors duration-200 transform lg:mt-0 lg:mx-4 hover:text-gray-900 dark:hover:text-gray-200">support</a>
				<a href="#" class="mt-2 transition-colors duration-200 transform lg:mt-0 lg:mx-4 hover:text-gray-900 dark:hover:text-gray-200">blog</a>
			</div>

			{#if mobileNav.isOpen}
				<div class="flex flex-col lg:hidden text-gray-600 capitalize dark:text-gray-300 lg:flex lg:px-16 lg:-mx-4 lg:flex-row lg:items-center">
					<a href="#" class="mt-2 transition-colors duration-200 transform lg:mt-0 lg:mx-4 hover:text-gray-900 dark:hover:text-gray-200">features</a>
					<a href="#" class="mt-2 transition-colors duration-200 transform lg:mt-0 lg:mx-4 hover:text-gray-900 dark:hover:text-gray-200">downloads</a>
					<a href="#" class="mt-2 transition-colors duration-200 transform lg:mt-0 lg:mx-4 hover:text-gray-900 dark:hover:text-gray-200">docs</a>
					<a href="#" class="mt-2 transition-colors duration-200 transform lg:mt-0 lg:mx-4 hover:text-gray-900 dark:hover:text-gray-200">support</a>
					<a href="#" class="mt-2 transition-colors duration-200 transform lg:mt-0 lg:mx-4 hover:text-gray-900 dark:hover:text-gray-200">blog</a>
				</div>
			{/if}

		</div>
	</div>
</nav>