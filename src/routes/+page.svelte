<svelte:head>
	<title>Home</title>
	<meta name="description" content="Home" />
</svelte:head>

<script>
	import Hero from "$lib/components/Hero.svelte";
	import Prodotti from "$lib/components/Prodotti.svelte";
	import FeatureProduct from "$lib/components/FeatureProduct.svelte";
</script>


<main>
	<Hero/>
	<Prodotti />
	<FeatureProduct />
</main>




