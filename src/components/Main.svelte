<script>
    import Step from './Step.svelte';

    let steps = [
        {name: 'Narrative Tracker App', icon: 'fa-brands fa-app-store-ios'}, 
        {name: 'Project Mercury Cohort 11', icon: 'fa-solid fa-lightbulb'}, 
        {name: 'USAF Training Program', icon: 'fa-solid fa-chart-line'}, 
    ]

    const skills = [
        {name: 'Python', level: 3},
        {name: 'SQL', level: 3},
        {name: 'Program Management', level: 4},
        {name: 'Data Analysis', level: 5},
        {name: 'Front End Dev', level: 2},
    ]

</script>

<style>
    .bar {
        background-color: #005B41;
        height: 20px;
        margin-bottom: 10px;
        border-radius: 4px;
    }
</style>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8
            lg:gap-10">
                <h2 class="font-semibold text -4xl sm:text-5xl md:text-6xl">
                    Hi! ✋ I'm <span class="Quicksand text-emerald-800">Joshua</span> Paul <br/>
                    <span class="Quicksand text-emerald-800">Innovator</span> & Business Analyst
                    

                </h2>
                <p class="text-base sm:text-lg md:text-xl">
                    Problem <span class="quicksand text-emerald-700"> solver</span>, Developer, <span class="quicksand text-emerald-700">and</span> Dad.
                </p>
        </div>
        <div class="relative shadow-lg grid place-items-center">
            <img src={"Josh.PNG"} alt="Profile"
            class="object-cover z-[2] max-h-[45vh] rounded-lg transition-shadow duration-300 ease-in-out hover:shadow-md"/>
        </div>

    </section>



    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my projects are: 
            </h6>
         </div>

         <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps [0]}> 
                <p>Narrative Tracker is a mobile app tailored for USAF members to conveniently track their achievements, streamlining the creation of their EPB/OPB. Originally developed with Swift and Firebase, I am currently transitioning to React Native for broader accessibility and scalability.
                </p>
            </Step>

            <Step step={steps [1]}> 
                <p>Within the Project Mercury ecosystem, I actively participated in a rigorous 13-week process involving numerous customer interviews and design sprints. This collaborative effort culminated in my team's conceptualization of the innovative term "Stand Off Cargo," intended to optimize cargo delivery systems within challenging operational environments.</p>
            </Step>

            <Step step={steps [2]}> 
                <p>Managed training data, scheduling, and funding for multiple squadrons. Tracked KPIs and training trends which culminated in being awarded the "Superior Performer Award". Utilized AF LMS, Excel, and PowerBi. </p>
            </Step>
         </div>
     </section>

     <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-28 md:gap-24 relative">
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0
            before:left-0 before:w-2/3 before:h-1.5 before:bg-emerald-800
            after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-emerald-800 py-4"> 

            <h3
                class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                 <span class="quicksand text-slate-100"> About me</span>
            </h3>
        </div>

        <div class="flex-col text-center overflowscroll gap-10 max-w-[800px] mx-auto w-full">
            <h5>
                With nine years of experience in data analysis within the USAF,
                 I bring a blend of precision and adaptability to every project. Currently I am working on my front-end development skills and diving into Mojo, 
                 I enjoy he challenge of mastering new technologies. As a passionate problem-solver fueled by coffee, 
                 I find joy in crafting innovative solutions. I work at North Spark Defense Lab where I focus rapid prototyping, SBIR facilitation, and course development.
            </h5>
        </div>

        <div class="w-full">
            {#each skills as skill}
            <div class="flex items center mb-2">
                <div class="w-1/4">
                    <p>{skill.name}</p>
                </div>
                <div class="w-3/4">
                    <div class="bg-slate-800 h-5 rounded">
                        <div class="bar bg-emerald-700" style="width: {skill.level * 20}%"></div>
                     </div>
                 </div>
            </div>
        {/each}

</div>

     </section>



</main>

