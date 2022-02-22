<script>
	function handleClick() {
		console.log('Thanks for pressing this button');
	}

	let theme = {
		primary:
			'bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 border border-blue-700 rounded transition ease-in duration-200 transform hover:-translate-y-1 active:translate-y-0',
		secondary:
			'bg-transparent hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded transition ease-in duration-200 transform hover:-translate-y-1 active:translate-y-0',
		v2: 'py-2 px-8 bg-transparent text-red-600 font-semibold border border-red-600 rounded hover:bg-red-600 hover:text-white hover:border-transparent transition ease-in duration-200 transform hover:-translate-y-1 active:translate-y-0',
        v3: 'bg-white text-gray-600 font-bold rounded border-b-2 border-green-500 hover:border-green-600 hover:bg-green-500 hover:text-white shadow-md py-2 px-6',
        v4: 'px-6 py-2 bg-black text-white rounded-lg font-bold transform hover:-translate-y-1 transition duration-400',
        v5: 'px-6 py-2 bg-transparent border border-black text-black rounded-lg font-bold transform hover:-translate-y-1 transition duration-400',
	};

	export let title = 'Click me!';
	export let url = null;
	export let type = 'primary';
</script>

{#if url}
	<a href={url} target="_blank" ref="nofollow">
		<button class={theme[type]} on:click={handleClick}>{title}</button>
	</a>
{:else}
	<button class={theme[type]} on:click={handleClick}>{title}</button>
{/if}
