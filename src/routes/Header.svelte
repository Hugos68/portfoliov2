<script lang="ts">
    type NavItem = { label: string; href: string; }

    const navItems: NavItem[] = [
        {
            label: 'Hugo Korte',
            href: '/'
        },
        {
            label: 'About',
            href: '/about'
        },
        {
            label: 'Work',
            href: '/work'
        },
        {
            label: 'Competence',
            href: '/competence'
        }
    ];
</script>

<header class="h-20 bg-gradient-to-r from-primary-500/50  to-secondary-500/25 m-2 rounded-token px-10">
    <nav class="h-full flex [&>*:nth-child(2)]:ml-auto 0 items-center gap-5 font-semibold text-lg">
        {#each navItems as {label, href}}
            <a href={href} class="px-3 py-2 hover:bg-surface-100/25 rounded-token transition-[background]">{label}</a>
        {/each}
    </nav>
</header>