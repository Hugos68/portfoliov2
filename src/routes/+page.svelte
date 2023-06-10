<script lang="ts">
	import { onMount } from "svelte";
	import { fly, scale } from "svelte/transition";

    type Project = {
        name: string;
        description: string;
        repositoryUrl: string;
        websiteUrl: string;
        imageUrl: string;
        technologies: string[]
    }
    
    const projects: Project[] = [
        {
            name: 'Subjective',
            description: 'An E-commerce web shop built for Subjective',
            repositoryUrl: 'https://github.com/SubjectiveTeam/subjective-website',
            websiteUrl: 'https://subjective-website.vercel.app/',
            imageUrl: 'https://cdn.discordapp.com/attachments/465110736872669195/1117202771645567036/image.png',
            technologies: ['SvelteKit', 'Skeleton', 'Tailwind', 'Supabase']
        },
        {
            name: 'Portfolio',
            description: 'A portfolio to showcase myself.',
            repositoryUrl: 'https://github.com/Hugos68/portfoliov2',
            websiteUrl: 'https://hugokorte.vercel.app/', 
            imageUrl: 'https://cdn.discordapp.com/attachments/465110736872669195/1117236476565016597/image.png',
            technologies: ['SvelteKit', 'Skeleton', 'Tailwind', 'Supabase']
        },
        {
            name: 'Peachess',
            description: 'A gaming platform to play chess on.',
            repositoryUrl: 'https://github.com/Hugos68/peachess',
            websiteUrl: 'https://peachess.vercel.app/', 
            imageUrl: 'https://cdn.discordapp.com/attachments/465110736872669195/1117228565004558396/image.png',
            technologies: ['SvelteKit', 'Skeleton', 'Tailwind', 'Supabase']
        }
    ];

    const undertitles: string[] = ['Dedicated software engineer.', 'Open source contributer.', 'Coffee addict.', 'Bachelors IT student.'];
    let undertitle: string = undertitles[0];
    onMount(() => {
        const interval = setInterval(() => {
            let newUndertitle: string;
            do {
                newUndertitle = undertitles[Math.floor(Math.random() * undertitles.length)];
            } while (newUndertitle === undertitle);
            undertitle = newUndertitle;
        }, 5000);
        return () => {
            clearInterval(interval);
        }
    });
</script>


<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('/green-wave-bottom.svg')] bg-cover bg-center">
    <h1 id="hugokorte" class="text-[clamp(2rem,16vw,4rem)] leading-[3] text-center">
        Hugo Korte
    </h1>
    {#key undertitle}
        <p class="text-[clamp(1.5rem,8vw,2rem)] text-dark-token text-center" in:scale|local={{ delay: 200 }} out:fly|local={{ y: 200, duration: 200 }}>{undertitle}</p>
    {/key}
</section>
<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('/green-wave-top.svg')] bg-cover bg-center">
    <h2 id="about" class="text-[clamp(2rem,16vw,4rem)] leading-[3]">
        About
    </h2>
</section>
<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('/blue-wave-bottom.svg')] bg-cover bg-center">

</section>  
<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('/blue-wave-top.svg')] bg-cover bg-center">
    <h2 id="work" class="text-[clamp(2rem,16vw,4rem)] leading-[3]">
        Work
    </h2>
    <ul class="grid grid-cols-1 xl:grid-cols-2 gap-8">
        {#each projects as project}
            <li class="card card-hover overflow-hidden group">
                <header class="overflow-hidden relative">
                    <img class="group-hover:scale-[1.1] group-hover:opacity-50 transition-[transform_opacity] duration-[250ms]" src={project.imageUrl} alt="{project.name}-image" />
                    <div class="absolute bottom-0 right-0 p-4 flex gap-2 justify-between">
                        {#each project.technologies as technology}
                            <p class="chip variant-filled opacity-0 group-hover:opacity-100 transition-opactity translate-y-20 group-hover:translate-y-0">{technology}</p>
                        {/each}
                    </div>
                </header>
                <div class="p-4 space-y-4">
                    <p class="text-lg font-bold">{project.name}</p>
                    <p>{project.description}</p>
                </div>
                <hr class="opacity-50" />
                <footer class="flex gap-2 justify-end p-4">
                    <a class="btn btn-sm variant-soft-secondary" href={project.repositoryUrl}>Source Code</a>
                    <a class="btn btn-sm variant-soft-tertiary" href={project.websiteUrl}>Live Preview</a>
                </footer>
            </li>
        {/each}
    </ul>
</section>
<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('/pink-wave-bottom.svg')] bg-cover bg-center">

</section>
<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('/pink-wave-top.svg')] bg-cover bg-center">
    <h2 id="competence" class="text-[clamp(2rem,16vw,4rem)] leading-[3]">
        Competence
    </h2>
</section>
<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('/green-wave-footer.svg')] bg-cover bg-center">
    
</section>
