<script>
    import Step from "./Step.svelte";

    let steps = [
        {name: 'Novel Nook', icon:'fa-solid fa-book', href: 'http://webhome.auburn.edu/~jeo0011/FinalProject/'},
        {name: 'State Your Claim', icon:'fa-solid fa-flag-usa', href: 'https://jackodom9.itch.io/state-your-business'},
        {name: 'Patent ChatBot', icon:'fa-solid fa-chalkboard-user'}
    ];

    let benefits = [
        {name: 'From an well-rounded engineering background:', description: 'I originally completed a bachelors in Chemical Engineering in 2020. During the course of that I worked as a Process Engineer for Freudenberg-NOK Sealing Technologies manufacturing sealing devices (O-rings, D-rings, Gaskets, etc.). After graduating, I was employed as a Patent Examiner by the United States Patent and Trademark Office, until I finally returned to college to pursue Computer Science. Throughout all of this I have learned both classroom and real life problem solving skills: doing intense mathematical work as a chemical engineering student, working with my hands on presses and machining tools at FNST, and parsing complex documentation regarding the law and new technologies every day examining Patent Applications. From all of this I have gained a holistic understanding of processes, and an ability to confidently tackle difficult problems, whatever form they may take.'},
        {name: 'Both University educated and self-taught:', description: 'While I loved the aspects of Patent Examining that involved learning about new innovations and learning as well as implementing the law in a logical way, I was feeling uninspired being a bureaucratic worker on the sidelines of innovation. I had several friends in the software industry share their work with me, and with that a passion was sparked. I began a journey of self-teaching to learn all that I could about the software development landscape. I quickly realized that computer science and software development were both too broad and too deep to easily learn on my own. From there I left my job and re-enrolled in college to gain a degree in Computer Science. I have thoroughly enjoyed every class I have taken and every additonal challenge I have encountered. Throughout my coursework I have supplemented it with developing my own personal projects, continued development of school projects to broaden their scope, as well as small coding challenges to exercise problem solving (Leetcode, Hackerrank, etc.), and other supplemental courses such as The Odin Project (Web Development Focused) to learn additional technologies.'},
        {name: 'Always striving to learn new things:', description: 'The one constant I have retained through my educational and work-related experience is the drive to constantly learn. Before attending college I asked mentors and other adults in my life what the most rigorous and comprehensive degree I could obtaion would be. The resounding answer was Chemical Engineering. I thoroughly enjoyed learning the many concepts taught that attempt to explain physical phenomena in the world around us, but I found that the employment opportunities offered just didn\'t align with my personal goals. Hearing that a career in intellectual property was an excellent way to stay at the forefront of innovation and constantly be exposed to new technologies I jumped in to pursue it. But I wasn\'t satisfied with just being a sideline player in the game to create. Realizing that the tech industry was both one of the fastest growing and most advanced industries really opened my eyes. Two years (and some change) in to learning about Computer Science and pursuing Software Development and I have not looked back once. I am certain I have found my passion and hope to find employment with a Company that is similar minded on the topic of expanding the horizon of what we all are capable of.'},
    ];
    
    function scrollToBottom() {
        const bottomElement = document.querySelector('#footer');

        
        bottomElement.scrollIntoView({ behavior: 'smooth' });
    }
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:6xl">
                Hi! I'm <span class="poppins" style="color: #E87722">Jack</span> Odom <br/> Aspiring
                <span class="poppins" style="color: #E87722">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span style="color: #E87722">favorite technologies</span> include web development tools (Javascript, PHP, SvelteKit),
                game development tools (Godot, Unity), as well as a variety of other technologies (Java, Python, SQL).
            </p>
            <a href="#" on:click={ scrollToBottom } class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950">
                <div class="absolute top-0 right-full w-full h-full bg-orange-400 opacity-20 group-hover:translate-x-full z-0 duration-200"></div>
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>
        <div class=" grid place-items-center">
            <img src={"images/profile.png"} alt='Jack Odom'class="object-cover z-[2] max-h-[70vh] border border-solid border-orange-400"/>
        </div>
    </section>


    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-orange-400">see</span> my work?
            </h3>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>Novel Nook is a simple, easy to use personal library system. It allows for the logging of books into different categories to keep tracks of books you own, have read, or want to read. It utilizes <strong class="text-orange-400">vanilla Javascript for the client-side,PHP for the server-side, and MySQL for a persistent database.</strong> Created for Auburn University's Web Development 2 Final Project.</p>
            </Step>
            <Step step={steps[1]}>
                <p>State Your Claim is an educational game aimed to teach and reinforce knowledge of American States and Capitals. It was created utilizing the <strong class="text-orange-400">Godot open-source game engine and was written in GDScript (a Python-Like Godot-specific language).</strong> The project was created for Auburn University's Game Development course.</p>
            </Step>
            <Step step={steps[2]}>
                <p>WIP</p>
            </Step>
        </div>
    </section>
    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-orange-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-orange-700 py-4">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                Want to Know more?
            </h6>
            <h3 class="font-semibold text-3l sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-orange-400">about</span> me.
            </h3>
            <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
                I am . . .
            </p>
            <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
                {#each benefits as benefit, index}
                    <div class="flex gap-6 sm:gap-8">
                        <p class="poppins text-4xl sm:text-5xl md:text-6x text-slate-500 font-semibold">
                            0{index+1}
                        </p>
                        <div class="flex flex-col gap-6 sm:gap-8">
                            <h3 class="text-2xl sm:text-3xl md:text-5xl">
                                {benefit.name}
                            </h3>
                            <p>{benefit.description}</p>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>
</main>