<script>
  export let y;

  let tabs = [
    { name: 'Projects', link: '#projects' },
    { name: 'About Me', link: '#about' },
  ]

</script>

<header class={'sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border border-solid ' + (
  y > 0 ? ' py-4 bg-sky-700 border-sky-700' : ' py-6 bg-transparent border-transparent'
)}>
  <h1 class="text-xl text-white">
    <b class="font-bold poppins text-white tracking-wide">Dan</b> June
  </h1>
  <div class="sm:flex ml-auto pr-4 items-center gap-4 hidden text-xl">
    {#each tabs as tab, index}
      <a href="{tab.link}" class="duration-200 hover:text-sky-400">
        <p class="text-white text-xl tracking-wide">{tab.name}</p>
      </a>
    {/each}
  <a href="#contact" class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-sky-950">
    <div class="absolute top-0 right-full w-full h-full bg-sky-400 opacity-20 group-hover:translate-x-full z-0 duration-200" />  
    <h4 class="relative z-9 text-sky-950">Get in touch</h4>
    </a>
  </div>
</header>