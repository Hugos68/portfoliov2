<script lang="ts">
    type NavItem = { label: string; href: string; }

    const navItems: NavItem[] = [
        {
            label: 'Hugo Korte',
            href: '#hugokorte'
        },
        {
            label: 'About',
            href: '#about'
        },
        {
            label: 'Work',
            href: '#work'
        },
        {
            label: 'Competence',
            href: '#competence'
        }
    ];

    let scrollY: number;
</script>

<svelte:window bind:scrollY  />

<header class="z-[111] sticky top-0 h-20 { scrollY > 50 ? "shadow-2xl bg-surface-700" : undefined} transition-[background_shadow] px-[1vw] lg:px-[10vw]">
    <nav class="h-full flex [&>*:nth-child(1)]:text-lg [&>*:nth-child(2)]:ml-auto 0 items-center gap-2 font-semibold">
        {#each navItems as {label, href}}
            <a href={href} class="px-3 py-2 hover:bg-surface-100/25 rounded-token transition-[background]">{label}</a>
        {/each}
    </nav>
</header>