<script>
	import { page } from '$app/stores';
	import { NAVIGATION_ELEMENTS } from '../constants/navigationElements';

	let mobileNav = { isOpen: false };

	function toggle() {
		mobileNav.isOpen = !mobileNav.isOpen;
	}
</script>

<nav class="flex justify-between p-8 bg-white">
	<a href="/" class="text-2xl">MyFirstApp</a>

	<div class="hidden justify-end md:block">
		{#each NAVIGATION_ELEMENTS as { href, title }, i}
			<span
				class="text-xl p-4 decoration-4 decoration-slate-500 hover:underline underline-offset-4 {$page
					.url.pathname === href
					? 'underline decoration-slate-700'
					: ''}"
			>
				<a {href}>
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
