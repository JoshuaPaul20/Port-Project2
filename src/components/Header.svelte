<script>
   export let y;  

   let tabs = [
    {name: 'Projets',  link: '#projects'},
    {name: 'About me', link: '#about'},

   ];
</script>

<header class={'sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border border-solid' + (
    y > 0 ? 'py-4 bg-stone-950 border-emerald-800' : 'py-6 bg-transprtent border-transparent'
)}>
    <h1 class="font-small">
        <img src="jlogo.png" alt="logo" style="width: 50px; height: auto;">
    </h1>
    
    <div class="sm:flex ml-auto pr-4 items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a href={tab.link} class="duration-200 hover:text-emerald-600">
            <p>{tab.name}</p>
             </a>
        {/each}
    </div> 
</header>


