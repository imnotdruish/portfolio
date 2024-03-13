<script>
  export let step;
</script>

<a href={step.href} target="_blank" class="p-4 sm:-6 md:p-8 flex flex-col gap-4 rounded-lg border border-solid border-sky-700 text-center group cursor-pointer hover:border-sky-400 duration-200">
  <div class="bg-transparent grid place-items-center p-4 text-5xl md:text-6xl mx-auto duration-200">
    <i class="{step.icon} text-purple-400 "/>
  </div>
  <h3 class="font-medium text-xl sm:text-2xl md:text-3xl text-sky-200">{step.name}</h3>
  <slot/>
  <div class="flex-1 flex justify-between gap-4 items-center">
    <div class="ml-auto cursor-pointer hover:text-sky-950 duration-200 relative after:absolute after:top-0 after:h-0 after:right-full after:w-full after:h-full after:bg-white after:duration-200 hover:after:translate-x-full after:z-[-1] overflow-hidden">
      <p class="relative z-4">Go to &rarr;</p>
    </div>
  </div>
</a>