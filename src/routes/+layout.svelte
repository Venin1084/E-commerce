<script>
	import Header from '$lib/components/Header.svelte';
	import MobileMenu from '$lib/components/MobileMenu.svelte';
	import '../app.css';

	/** @type {{children: import('svelte').Snippet}} */
	let { children } = $props();
</script>

<!-- Menu Mobile (si apre quando $openModal è true) -->
<MobileMenu />

<div class="app">
	
	<Header />

	<main>
		<!-- This is were the components -->
		{@render children()}
	</main>

	<footer>
		<p>
			this is a footer
		</p>
	</footer>
</div>