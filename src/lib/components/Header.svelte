<script>
	import { page } from '$app/state';/* gia di svlete kit */
	import { openModal } from "../stores/index";
</script>

<header class="flex flex-col relative z-20 lg:px-67 bg-gray-100 ">
	<div class="max-w-[1400px] mx-auto w-full flex items-center justify-between p-4 py-6">
		<!-- Logo -->
		<a href="/">
			<h1 class="font-semibold sm:px-2">
				Arbor Home
			</h1>
		</a>

		<!-- Desktop Navigation -->
		<nav class="hidden md:flex items-center gap-4 lg:gap-6 ">
			<ul class="flex gap-6">
				
				<li aria-current={page.url.pathname === '/prodotti' ? 'page' : undefined}>
					<a href="/prodotti">Prodotti</a>
				</li>
			
				<li aria-current={page.url.pathname === '/about' ? 'page' : undefined}>
					<a href="/about">About</a>
				</li>
				<li aria-current={page.url.pathname === '/contatti' ? 'page' : undefined}>
					<a href="/contatti">Contatti</a>
				</li>
			</ul>
		</nav>

		<!-- Mobile-->
		<div class="flex items-center gap-4 md:hidden px-10">
			<!-- Hamburger Menu Button -->
			<button
				onclick={() => ($openModal = true)}
				class="grid place-items-center"
				aria-label="Apri menu"
			>
				<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-menu">
					<path d="M4 5h16"/>
					<path d="M4 12h16"/>
					<path d="M4 19h16"/>
				</svg>
			</button>
			
			<!-- Cart Icon per Mobile -->
			<a href="/carrello" class="grid place-items-center" aria-label="Vai al carrello">
				<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-shopping-cart">
					<circle cx="8" cy="21" r="1"/>
					<circle cx="19" cy="21" r="1"/>
					<path d="M2.05 2.05h2l2.66 12.42a2 2 0 0 0 2 1.58h9.78a2 2 0 0 0 1.95-1.57l1.65-7.43H5.12"/>
				</svg>
			</a>
		</div>

		<!-- Desktop posizonata apposta -->
		<a href="/carrello" class="hidden md:grid place-items-center" aria-label="Vai al carrello">
			<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-shopping-cart">
				<circle cx="8" cy="21" r="1"/>
				<circle cx="19" cy="21" r="1"/>
				<path d="M2.05 2.05h2l2.66 12.42a2 2 0 0 0 2 1.58h9.78a2 2 0 0 0 1.95-1.57l1.65-7.43H5.12"/>
			</svg>
		</a>
	</div>
</header>