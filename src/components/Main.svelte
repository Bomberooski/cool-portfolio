<script>
    import Step from "./Step.svelte";

    let steps = [
        {name: 'Todo List For You', icon: 'fa-solid fa-square-check', href: "https://seansreacttodolist.netlify.app/"},
        {name: 'Sean Widmer Podcast', icon: 'fa-solid fa-headphones', href: "https://seanslife.com/podcast"},
        {name: 'The Final Frontier', icon: 'fa-solid fa-shuttle-space', href: "https://the-nasa-picture-of-the-day.netlify.app/"},
        {name: 'Game Time', icon: 'fa-solid fa-dice', href: "https://seanstenzies.netlify.app/"}

    ]

    let benefits = [
        { name: 'a self taught developer', description: 'After a 20 year career in radio I decided on a change and after diving into a bunch of online resources I fell in love with coding. The oppurtunity to take a blank canvas and transform it into something cool and interactive resonated with me in a big way. I started the journey with basic Javascript, HTML and CSS and then dove into other Javascript frameworks, design, cloud services, AI and so much more.'},
        { name: 'a product design and UX fanatic', description: 'Creating unique, attractive and fun user experiences allowed me to take my decades of daily radio creativity and transfer that skill into building on the web. The challenge of learning new design concepts so that I can share that experience with users has become a passion of mine.'},
        { name: 'an excellent communicator', description: 'Communication has a will always be a core value I hold on to tightly. Whether it is with co-workers, consumers, friends or family, taking the time to communicate well is something I find to be crucial in the success of any relationship. It\'s something I am proud to bring to any workspace.'},
        
    ]

</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-zinc-400">Sean</span> Widmer <br /> Web <span class="poppins text-zinc-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-zinc-400">favorite tech</span> includes React, JavaScript (NEXT.JS or SvelteKit), TailwindCSS, Node.js + Express.js & PostgreSQL or Firebase/Firestore!
            </p>
            <a 
                href="https://www.linkedin.com/in/sean-widmer-98113730/"
                target="_blank"
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-emerald-950 cursor-pointer"
            >
                <div class="absolute top-0 right-full w-full h-full bg-zinc-400 opacity-20 group-hovewr:translate-x-full z-0 duration-200" 
                />
                    <h4 class="relate z-9">Get in touch  &rarr;</h4>
                
            </a>
        </div>
        <div class="relative  grid place-items-center">
            <img src={"images/profile.png"} alt="Profile_image" class="object-cover z-[2] max-h-[70vh]" />
        </div>
    </section>



    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-zinc-400">see</span> my work?
            </h3>
        </div>
        <a href="https://github.com/Bomberooski"
            target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-zinc-600 
            flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-zinc-400 duration-200">
            <i class="fa-regular fa-circle-play"></i>
            <p>Check it out</p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-4 gap-12 lg:gap-10" >
            <Step step={steps[0]}>
                <p>Everyone needs to give podcasting a try! <strong class="text-zinc-400"> So here is a todo list for you to use</strong> to make sure you achieve your podcasting goals. <br /><br /> It can also be a powerful tool to use to save potential segment ideas.</p>
            </Step>
            <Step step={steps[1]}>
                <p>Check out my personal podcast here. <strong class="text-zinc-400">Well over 500 episodes</strong> are currently available for your ears to absorb.</p>
            </Step>
            <Step step={steps[2]}>
                <p>Space is after all <strong class="text-zinc-400">THE FINAL FRONTIER</strong>. Take a moment to check out a <strong class="text-zinc-400">Picture Of The Day</strong> from NASA and learn something about the vast universe!</p>
            </Step>
            <Step step={steps[3]}>
                <p>If you know me you know <strong class="text-zinc-400">I love games</strong> and I couldn't let you browse this site without the oppurtunity to play something. Here's a game call <strong class="text-zinc-400">"Tenzies"</strong> for you to get after (I think my personal record is 7).</p>
            </Step>
        </div>
    </section>

    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16
    sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0
        before:left-0 before:w-2/3 before:h-1.5 before:bg-zinc-600 after:absolute after:bottom-0
        after:right-0 after:w-2/3 after:h-1.5 after:bg-zinc-600 py-4">
            <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-zinc-400">about</span> me.
            </h3>
        </div>
        <p class='mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl'>I am . . . </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-x-[800px]">
            {#each benefits as benefit, index}
            <div class="flex gap-6 sm:gap-8">
                <p class="poppins text-4xl sm:text-5xl md:text-6xl text-emerald-400 font-semibold">
                    0{index+1}
                </p>
                <div class="flex flex-col gap-6 sm:gap-8">
                    <h3 class="text-2xl sm:text-3xl md:text-5xl">
                        {benefit.name}
                    </h3>
                    <p>
                        {benefit.description}
                    </p>
                </div>
            </div>
            {/each}
        </div>
        <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">The <span class="text-zinc-400 poppins">Complete</span> Pacakage</h5>
        <div 
            class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
        >
            <table class="bg-white text-emerald-700 rounded text-center">
                <thead class="border-b border-solid border-emerald-200">
                    <tr class="">
                        <th />
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th class="whitespace-nowrap bg-zinc-700 text-white p-4 px-8">Me</th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-emerald-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Dedication</td>
                        <td><i class="fa-solid fa-check text-emerald-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-emerald-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-emerald-500"></i></td>
                        <td><i class="fa-solid fa-check text-blue-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-emerald-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Critical Thought</td>
                        <td><i class="fa-solid fa-xmark text-emerald-500"></i></td>
                        <td><i class="fa-solid fa-check text-emerald-500"></i></td>
                        <td><i class="fa-solid fa-check text-emerald-500"></i></td>
                        <td><i class="fa-solid fa-check text-blue-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-emerald-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Interpersonal Skills</td>
                        <td><i class="fa-solid fa-check text-emerald-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-emerald-500"></i></td>
                        <td><i class="fa-solid fa-check text-emerald-500"></i></td>
                        <td><i class="fa-solid fa-check text-blue-500"></i></td>
                    </tr>
                    <tr class="border-solid border-emerald-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Programming Ability</td>
                        <td><i class="fa-solid fa-xmark text-emerald-500"></i></td>
                        <td><i class="fa-solid fa-check text-emerald-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-emerald-500"></i></td>
                        <td><i class="fa-solid fa-check text-blue-500"></i></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        <p class="mx-auto">So why not invest?</p>
    </section>
</main>