<script>
	import '../../app.css';
	import Navigation from '../../components/Navigation.svelte';
	import Footer from '../../components/Footer.svelte';
</script>

<div class="mx-auto xl:w-8/12 lg:w-10/12">
	<div class="flex flex-col min-h-screen">
		<header>
			<Navigation/>
		</header>
		<main class="flex flex-grow">
			<slot/>
		</main>
		<Footer/>
	</div>
</div>