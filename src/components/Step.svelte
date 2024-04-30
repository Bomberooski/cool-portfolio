<script>
    export let step;
</script>

<div class="p-4 sm:p-6 md:p-8 flex flex-col
gap-4 rounded-lg border border-solid border-zinc-700 text-center group 
 hover:border-zinc-400 duration-200">
    <div class="bg-emerald-900 grid place-items-center px-4 text-5xl md:text-6xl -mt-10 sm:-mt-12 md:-mt-14 lg:-mg-16 mx-auto duration-200">
        <i class={step.icon} />
    
    </div>
    <h3 class="font-medium text-xl sm:text-2xl md:text-3xl">{step.name}</h3>
    <slot/>
    <div class="flex:1 flex justify-between gap-4  items=center">
        <div class="ml-auto cursor-pointer hover:text-emerald-900 duration-200 
        relative after:absolute after:top-0 after:h-0 after:right-full
        after:w-full after:h-full  after:bg-white after:duration-200 hover:after:translate-x-full after:z-[-1]
        overflow-hidden">
            <a class="relative z-4" href={step.href} target="_blank">Go to &rarr;</a>
        </div>
    </div>
</div>