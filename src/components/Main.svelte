<script>
  import Step from './Step.svelte';

  let steps = [
    {name:'Pokédex', icon: 'fa-solid fa-diagram-project'},
    {name:'Coming Soon', icon: 'fa-solid fa-list-check'},
    {name:'Coming Soon', icon: 'fa-solid fa-diagram-project'},
  ]

  let benefits = [
    {name:'a self taught developer', description: 'I learned coding through onlnie resources and love creating and developing experiences with the user in mind. I started with HTML, CSS, and JavaScript and have been broadening my knowledge into backend development.'},
    {name:'a sponge for knowledge', description: 'I hate to give no as an answer. If there is a better way to do something, I want to learn about it and grow my knowledge for the future. If I can create something for someone that solves a problem they have, that is the best thing in the world.'},
    {name:'an execellent communicator', description: 'Being able to communicate with your everyone is key, regardless if it\'s a client or a peer. I have spent years in retail sales along with speaking in front of hundreds of people for trainings, on-boardings, and public events. Knowing what to say pending on who the audience is can be the difference between success and failure.'},
  ]
</script>

<main class="flex flex-col flex-1 p-4">
  <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
    <div class="relative grid place-items-center">
      <img src={"images/profile.png"} alt="Dan June" class="object-cover z-[2] max-h-[50vh]"/>
      </div>
      <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">        
        <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
          Hi! I'm Dan June <br/> Front End Developer
        </h2>
        <p class="text-base sm:text-lg md:text-xl">
          My favorite tech includes JavaScript (REACT.js or SvelteKit), TailwindCSS, Node.js + Express.js & PostgreSQL or Firebase/Firestore!
        </p>
      <a href="#contact" class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-sky-950 cursor-pointer">
        <div class="absolute top-0 right-full w-full h-full bg-sky-400 opacity-20 group-hover:translate-x-full z-0 duration-200">
      
        </div> 
        <h4 class="relative z-9 text-sky-950">Get in touch &rarr;</h4>
      </a>
    </div>
  </section>
  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-large sm:text-xl md:text-2xl">
        A few of my creative endeavors.
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Curious to see my work?
      </h3>
    </div>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>Pokemon App is a HTML, CSS, JavsScript web application, hosted on Netlify, that catches the Pokemon API to display all information about a Pokemon.</p>  
      </Step>
      <Step step={steps[1]}>
        <p>Coming Soon!!</p>
      </Step>
      <Step step={steps[2]}>
        <p>Coming Soon!!</p>        
      </Step>
    </div>
  </section>
  <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
    <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-purple-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-purple-700">
      <h6 class="text-lg sm:text-xl md:text-2xl pt-4">Want to know more?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl pb-4">
        A bit <span class="poppins text-purple-600">about</span> me.</h3>
      </div>
      <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .
      </p>
      <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
        {#each benefits as benefit, index}
          <div class="flex gap-6 sm:gap-8">
            <p class="poppins text-4xl sm:text-5xl md:text-6xl text-purple-600 font-semibold">
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
      <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
        <p>Scroll to see more &rarr;</p>
      </div>
      <p class="mx-auto text-2xl sm:text-3xl">So why not invest?</p>
  </section>
</main>