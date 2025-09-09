<script lang="ts">
  import { ArrowUpRight } from "lucide-svelte";

  import Seo from "$lib/components/Seo.svelte";
</script>

<Seo
  title="Andrei Staicu"
  description="Reseracher in theoretical computer science."
/>

<p
  class="layout-md text-black text-xl leading-tight font-light mb-8"
  id="andrei-is"
>

<div class="layout-md text-lg space-y-8">
  <div class="space-y-5">
    <p>
      I am a Computer Science PhD student at the <a class="link" href="https://siebelschool.illinois.edu/research/areas/theory-and-algorithms">University of Illinois</a>, where I am advised by <a class="link" href="https://miforbes.cs.illinois.edu/">Prof. Michael Forbes</a>.
    </p>

    <p>
      My research interests are in theoretical computer science, specifically algebraic complexity theory, coding theory, 
      and randomness in computation. I am interested in exploring the connections between algebraic geometry and computer science.
    </p>

    <p>
      Previously, I was a research assistant at <a class="link" href="https://laber-labs.com/">Laber Labs</a>, advised by Prof. Eric Laber. I completed my undergrad at 
      Caltech in Mathematics with a minor in Computer Science. I was fortunate to be advised by and work on research projects under the guidance 
      of Prof Schulman and Prof Umans. This is my <a href="/assets/pdf/resume.pdf" target="_blank" rel="noopener noreferrer" class="underline">CV</a>, 
      my publications are listed under <a href="/research" class="underline">research</a>, and I have my email and other information in the <a href="/extras" 
      class="underline">extras</a> tab. 
    </p>
  </div>

</div>

<style lang="postcss">
  .g {
    @apply text-neutral-400;
  }

  em {
    @apply font-serif text-[110%] leading-[100%];
  }

  .project-pair {
    @apply grid sm:grid-cols-[3fr,2fr] gap-y-1 -mx-3 px-3 py-2 hover:bg-neutral-100 transition-colors;
  }

  aside {
    @apply mt-0.5 text-base text-neutral-500;
  }

  /* Correction for vertical navigation links on mobile. */
  @media (max-width: 420px) {
    #andrei-is {
      @apply -mt-10;
    }
  }
</style>
