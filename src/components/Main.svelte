<script>
    import Step from "./Step.svelte";
    let steps=[
        {name: 'Akinator', icon: 'fa-solid fa-question'},
        {name: 'Autoclicker', icon: 'fa-solid fa-computer-mouse'},
        {name: 'Suika', icon: 'fa-solid fa-gamepad'}
    ]

    let things=[
        {name: 'I am a ftc programmer', des: 'In 9th grade i joined info(1)robotics, my schools robotics team, and i started programming bots'},
        {name: 'I am a curious person', des: 'I consider myself a person that is thirsty for knowledge and I hope to grow both personally and professionally '},
        {name: 'I like to play basketball', des: 'I played basketball for clubs, and i enjoy competing  with others, not only in sports'},

]
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi I'm <span class="text-gray-600">Nichita</span> Andrei<br/>Upcoming
                <span class="text-gray-600">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-gray-600">fav tech</span> includes Java and Javascript,TailwindCSS, Svelte and others
            </p>
            
            <a class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl 
            relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"href="https://www.instagram.com/anvrxi/" target="_blank"> 
                 <div
                class="absolute top-0 right-full w-full h-full bg-gray-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                 />
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>

        <div class="relative shadow-2xl grid place-items-center"> 
            <img src={"images/Logo.png"} alt="Logo" class="object-coverz-[2] max-h-[70vh]"/>
            </div>

    </section>



    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h3 class="font-semibold text-2xl sm:text-3xl md:text-4xl">
                Some of <span class="text-gray-600"> my</span> projects    
            </h3>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>Akinator game that guesses the <span class="text-gray-400">robotics team that you tough of</span> - made for 2024 regio</p>
            </Step>
            <Step step={steps[1]}>
                <p>Undetectable autoclicker for <span class="text-gray-400">minecraft pvp</span> - works best in versions lower than 1.9 because of the combat update</p>
            </Step>
            <Step step={steps[2]}>
                <p>Suika inspired game <span class="text-gray-400">with my classmates</span> - tic classes were boring</p>
            </Step>
        </div>

    </section>


    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative ">
        <div class="flex flex-col gap-4 text-center relative before:relative before:top-0 before:left-0 before:w-3/3
        before:h-1.5  before:bg-gray-700  after:relative after:top-0 after:left-0 after:w-3/3
        after:h-1.5  after:bg-gray-700 py-4">
         
         <h3 class="font-semibold text-3xl sm:text-4xl">
            More <span class="text-gray-700">things </span>about me
        </h3>
    </div>

    <div class= "flex flex-col gap-20 w-full mx-auto max-w-[800px]">
        {#each things as thing , index}
            <div class="flex gap-6 sm:gap-8">
                <p class="text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                    0{index+1}
                </p>
                <div class="flex flex-col gap-6  sm:gap-8">
                    <h3 class="text-2xl sm:-text-3xl md:text-5xl">
                        {thing.name}
                    </h3>
                    <p>{thing.des}</p>
                </div>
            </div>
        {/each}
    </div>

    </section>
</main>