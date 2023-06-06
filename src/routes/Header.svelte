<script lang="ts">
    let scrollY: number;
</script>
<svelte:window bind:scrollY />

<header class="sticky {scrollY > 50 ? "h-20 px-[5vw] md:px-[20vw] bg-white text-black" : "h-36 px-[5vw] bg-black text-white"} transition-[background,height,padding,color] duration-[350ms] top-0 flex items-center justify-between">
    <a href="#home" class="text-2xl font-extrabold">Hugo Korte</a>
    <nav class="font-bold flex items center gap-4">
        <a href="#about">About</a>
        <a href="#work">Work</a>
        <a href="#skillset">Skillset</a>
    </nav>
</header>