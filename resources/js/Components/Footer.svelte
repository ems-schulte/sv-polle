<script>
    import CookieSettingsButton from './CookieSettingsButton.svelte';

    export let footerItems;
    const currentYear = new Date().getFullYear();
</script>

<footer class="bg-gray-100 dark:bg-gray-950">
    <div class="max-w-7xl mx-auto py-4 px-4 sm:px-6 lg:px-8">
        <ul class="hidden lg:flex justify-center gap-4 mb-2">
            {#each footerItems as item}
                <li>
                    <a
                        href={item.href}
                        class="text-sm text-gray-900 dark:text-gray-100 hover:underline"
                    >
                        {item.text}
                    </a>
                </li>
            {/each}
            <li>
                <CookieSettingsButton buttonStyle="text-sm" />
            </li>
        </ul>
        <p class="text-center text-gray-900 dark:text-gray-100">© {currentYear} SV Polle</p>
    </div>
</footer>
