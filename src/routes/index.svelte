<script context="module">
	export const prerender = true;
</script>

<script>
	import Search from '$lib/Search.svelte';
	import AddButton from '$lib/AddButton.svelte';
	import CardList from '$lib/CardList.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<Search />
	<CardList />
</section>

<AddButton />

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: space-around;
		align-items: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
