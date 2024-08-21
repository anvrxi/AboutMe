<script>
    export let step;
</script>

<a href={step.href} target="blank" class="p-4 sm:p-6 md:p-8 flex flex-col gap-4 rounded-lg border border-solid border-gray-500 text-center group cursor-pointer hover:border-gray-200 duration-200">

    <div class="bg-white grid place-items-center px-4 text-5xl md:text-6xl -mt-10 sm:-mt-12 md:-mt-14 lg:-mt-16 mx-auto duration-200">
        <i class={step.icon}></i>
    </div>

    <!-- Added margin-top to lower the step.name -->
    <h3 class="font-medium text-xl sm:text-2xl md:text-3xl mt-4 sm:mt-6 md:mt-8">
        {step.name}
    </h3>

    <slot/>

    <div class="flex-1 flex justify-between gap-4 items-center">
        <div class="ml-auto cursor-pointer hover:text-gray-950 duration-200 relative after:absolute after:top-0 after:h-0 after:right-full after:w-full after:h-full after:bg-gray-400 after:duration-200 hover:after:translate-x-full after:z-[-1] overflow-hidden">
            <a href="https://github.com/anvrxi" class="relative z-[4]">
                <button class="px-4 py-2 bg-gray-800 text-white rounded hover:bg-gray-600 duration-200">
                    Go to &rarr;
                </button>
            </a>
        </div>
    </div>

</a>