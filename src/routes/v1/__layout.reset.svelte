<script>
	import '../../app.css';
	import Navigation from '../../components/Navigation.svelte';
	import Footer from '../../components/Footer.svelte';
</script>

<div class="mx-auto max-w-6xl xl:w-7/12 lg:w-10/12">
	<div class="flex flex-col min-h-screen">
		<header>
			<Navigation />
		</header>
		<main class="flex flex-grow">
			<div class="p-8 w-full">
				<slot />
			</div>
		</main>
		<Footer />
	</div>
</div>
