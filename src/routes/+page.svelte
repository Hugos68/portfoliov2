<script lang="ts">
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
            description: 'An online web shop built for Subjective',
            repositoryUrl: 'https://github.com/SubjectiveTeam/subjective-website',
            websiteUrl: 'https://subjective-website.vercel.app/',
            imageUrl: 'https://cdn.discordapp.com/attachments/465110736872669195/1117202771645567036/image.png',
            technologies: ['SvelteKit', 'Skeleton', 'Tailwind', 'Supabase']
        }
    ]
</script>


<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('green-wave-bottom.svg')] bg-cover bg-center">
    <h1 id="hugokorte" class="text-[clamp(2rem,16vw,4rem)] leading-[3] text-center">
        Hugo Korte
    </h1>
    <p class="text-[clamp(1.5rem,8vw,2rem)] text-dark-token text-center">A dedicated software engineer</p>
</section>
<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('green-wave-top.svg')] bg-cover bg-center">
    <h2 id="about" class="text-[clamp(2rem,16vw,4rem)] leading-[3]">
        About
    </h2>
</section>
<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('blue-wave-bottom.svg')] bg-cover bg-center">

</section>  
<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('blue-wave-top.svg')] bg-cover bg-center">
    <h2 id="work" class="text-[clamp(2rem,16vw,4rem)] leading-[3]">
        Work
    </h2>
    <ul class="grid grid-cols-1 lg:grid-cols-2">
        {#each projects as project}
            <li class="card card-hover overflow-hidden group">
                <header class="overflow-hidden">
                    <img class="group-hover:scale-[1.1] transition-transform duration-[250ms]" src={project.imageUrl} alt="{project.name}-image" />
                </header>
                <div class="p-4 space-y-4">
                    <p class="text-lg font-bold">{project.name}</p>
                    <p>{project.description}</p>
                </div>
                <hr class="opacity-50" />
                <footer class="flex justify-between p-4">
                    <div class="flex gap-3">
                        <a class="btn btn-sm variant-soft-primary" href={project.websiteUrl}>Live Preview</a>
                        <a class="btn btn-sm variant-soft-primary" href={project.repositoryUrl}>Source Code</a>
                    </div>
                    <div class="flex gap-3">
                        {#each project.technologies as technology}
                            <p class="chip variant-filled">{technology}</p>
                        {/each}
                    </div>
                </footer>
            </li>
        {/each}
    </ul>
</section>
<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('pink-wave-bottom.svg')] bg-cover bg-center">

</section>
<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('pink-wave-top.svg')] bg-cover bg-center">
    <h2 id="competence" class="text-[clamp(2rem,16vw,4rem)] leading-[3]">
        Competence
    </h2>
</section>
<section class="w-screen h-screen pt-[20vh] px-[2vw] lg:px-[10vw] bg-[url('green-wave-footer.svg')] bg-cover bg-center">
    
</section>
