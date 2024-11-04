<script>
    import Step from "./Step.svelte";
    let steps = [
        { name: 'Akinator', icon: 'fa-solid fa-question' },
        { name: 'Autoclicker', icon: 'fa-solid fa-computer-mouse' },
        { name: 'Suika', icon: 'fa-solid fa-gamepad' }
    ];

    let things = [
        { name: 'I am an FTC programmer', des: 'In 9th grade, I joined my school’s robotics team and started programming bots.' },
        { name: 'I am a curious person', des: 'Thirsty for knowledge, I aim to grow both personally and professionally.' },
        { name: 'I like to play basketball', des: 'I enjoy competing with others, both in sports and beyond.' }
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl leading-tight animate-fadeIn">
                Hi, I'm <span class="text-gray-600">Nichita Andrei</span><br/>Upcoming
                <span class="text-gray-600">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl animate-slideIn">
                My <span class="text-gray-600">favorite tech</span> includes Java, JavaScript, TailwindCSS, Svelte, and Bootstrap.
            </p>
            <a class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer hover:shadow-lg transition duration-200"
                href="https://www.instagram.com/anvrxi/" target="_blank">
                <div class="absolute top-0 right-full w-full h-full bg-gray-400 opacity-20 group-hover:translate-x-full transition duration-300"></div>
                <h4 class="relative z-10">Get in touch &rarr;</h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src="images/Logo.png" alt="Logo" class="object-cover max-h-[70vh] transform transition hover:scale-105" />
        </div>
    </section>

    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h3 class="font-semibold text-2xl sm:text-3xl md:text-4xl">
                Some of <span class="text-gray-600">my</span> projects
            </h3>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>Bootstrap template <span class="text-gray-400">trying to develop an intuitive template</span> for people that want to learn bootstrap - in progres</p>
            </Step>
            <Step step={steps[1]}>
                <p>This site's repository <span class="text-gray-400">on github</span> - the code can be easily edited for yourself</p>
            </Step>
            <Step step={steps[2]}>
                <p>Suika inspired game, reworked <span class="text-gray-400"> better phisics and neon UI </span> - i was bored</p>
            </Step>
        </div>
    </section>

    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-4 text-center relative before:absolute before:top-0 before:left-1/2 before:transform before:-translate-x-1/2 before:w-2/3 before:h-1 before:bg-gray-700 py-4">
            <h3 class="font-semibold text-3xl sm:text-4xl">
                More <span class="text-gray-700">things</span> about me
            </h3>
        </div>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each things as thing, index}
                <div class="flex gap-6 sm:gap-8 items-start">
                    <p class="text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold animate-fadeIn">
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-4 sm:gap-6 animate-slideIn">
                        <h3 class="text-2xl sm:text-3xl md:text-4xl font-medium text-slate-800">
                            {thing.name}
                        </h3>
                        <p class="text-lg sm:text-xl text-slate-600">
                            {thing.des}
                        </p>
                    </div>
                </div>
            {/each}
        </div>
    </section>
</main>

<style>
    @keyframes fadeIn {
        from { opacity: 0; }
        to { opacity: 1; }
    }
    @keyframes slideIn {
        from { transform: translateX(-10px); opacity: 0; }
        to { transform: translateX(0); opacity: 1; }
    }
    .animate-fadeIn { animation: fadeIn 0.5s ease-out both; }
    .animate-slideIn { animation: slideIn 0.5s ease-out both; }
</style>
