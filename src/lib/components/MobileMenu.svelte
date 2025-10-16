<!-- Versione Mobile dellla navigazione la humburger emnu e basato su un bolleano -->

<script>
    import { page } from '$app/state';
    import { openModal } from "../stores/index";

    const navItems = [
        { href: '/', label: 'Home' },
        { href: '/prodotti', label: 'Prodotti' },
        { href: '/checkout', label: 'Checkout' },
        { href: '/about', label: 'About' },
        { href: '/contatti', label: 'Contatti' },
    ];

    function closeMenu() {
        $openModal = false;
    }
</script>
<!--IF -->
{#if $openModal}
    <!-- Overlay -->
    <div
        on:click={closeMenu}
        on:keydown={(e) => e.key === 'Escape' && closeMenu()}
        class="fixed inset-0 bg-black/50 z-40 md:hidden transition-opacity duration-300"
        role="button"
        tabindex="0"
        aria-label="Chiudi menu"
    ></div>

    <!-- Sidebar -->
    <div
        class="fixed top-0 right-0 h-screen w-[60%] max-w-sm bg-white z-50 flex flex-col shadow-2xl md:hidden transform transition-transform duration-300 ease-out"
    >
        <!-- Header -->
        <div class="flex items-center justify-end gap-4  p-5 ">
          
            <button
                on:click={closeMenu}
                class="outline-none border-none p-2 hover:bg-gray-100 rounded-full transition-colors "
                aria-label="Chiudi menu"
            >
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <path d="M18 6 6 18"/>
                    <path d="m6 6 12 12"/>
                </svg>
            </button>
        </div>

        <!-- Navigation -->
        <nav class="flex flex-col flex-1 p-5 px-6">
            <ul class="flex flex-col gap-2">
                <!-- FOREACH -->
                {#each navItems as item}
                    <li>
                        <a 
                            href={item.href}
                            on:click={closeMenu}
                            class="block p-3 rounded-lg hover:bg-indigo-50 transition-colors duration-200"
                            class:bg-indigo-100={page.url.pathname === item.href}
                        >
                            <span class="text-lg font-medium">{item.label}</span>
                        </a>
                    </li>
                {/each}
            </ul>
        </nav>

    </div>
{/if}