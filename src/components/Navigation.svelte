<script>
	import { page } from '$app/stores';
	import { NAVIGATION_ELEMENTS } from '../constants/navigationElements';

	let mobileNav = { isOpen: false };

	function toggle() {
		mobileNav.isOpen = !mobileNav.isOpen;
	}
</script>

<nav class="bg-white flex justify-between m-8">
	<a href="/" class="text-2xl">MyFirstApp</a>

	<div class="hidden md:flex">
		{#each NAVIGATION_ELEMENTS as { href, title }, i}
			<span>
				<a
					{href}
					class="text-slate-500 ml-8 text-xl decoration-4 hover:underline hover:decoration-slate-300 underline-offset-4 {$page
						.url.pathname === href
						? 'text-slate-900 underline decoration-slate-500 hover:decoration-slate-500'
						: ''}"
				>
					{title}
				</a>
			</span>
		{/each}
	</div>

	<div class="flex md:hidden" on:click={toggle}>
		<button
			type="button"
			class="text-black hover:text-gray-600 focus:outline-none focus:text-gray-600"
			aria-label="toggle menu"
		>
			<svg viewBox="0 0 20 20" class="w-6 h-6 fill-current">
				<path
					fill-rule="evenodd"
					d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
				/>
			</svg>
		</button>
	</div>
</nav>
{#if mobileNav.isOpen}
	<div class="flex flex-col md:hidden text-right p-8">
		{#each NAVIGATION_ELEMENTS as { href, title }, i}
			<span
				on:click={toggle}
				class="text-xl font-bold py-4 pr-4 text-gray-700 border-b border-gray-100 hover:bg-gray-50 md:hover:bg-transparent md:border-0 md:p-0"
			>
				<a class="w-full" {href}>
					{title}
				</a>
			</span>
		{/each}
	</div>
{/if}
