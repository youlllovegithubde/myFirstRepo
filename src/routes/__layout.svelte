<script>
	import '../app.css';
	import Navigation from '../components/Navigation.svelte';
	import Sidebar from '../components/Sidebar.svelte';
	import Footer from '../components/Footer.svelte';
</script>

<div class="mx-auto max-w-6xl xl:w-7/12 lg:w-10/12">
	<div class="flex flex-col min-h-screen">
		<header>
			<Navigation />
		</header>
		<main class="flex flex-grow">
			<div class="md:w-2/3 p-8">
				<slot />
			</div>
			<div class="hidden md:block w-1/3 p-8">
				<Sidebar />
			</div>
		</main>
		<Footer />
	</div>
</div>
