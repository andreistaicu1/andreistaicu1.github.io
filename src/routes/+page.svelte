<script lang="ts">
  import { ArrowUpRight } from "lucide-svelte";

  import Seo from "$lib/components/Seo.svelte";

  const featuredProjects = [
    {
      name: "Identifiability of Product of Experts Models",
      href: "https://arxiv.org/abs/2310.09397?context=math.AG",
      desc: "arXiv pre-print",
    },
  ];
</script>

<Seo
  title="Andrei Staicu"
  description="Reseracher in theoretical computer science."
/>

<p
  class="layout-md text-black text-xl leading-tight font-light mb-16"
  id="andrei-is"
>

<div class="layout-md text-lg space-y-14">
  <div class="space-y-5">
    <p>
      I am an undergraduate at Caltech studying math.
    </p>

    <p>
      My research interests are in theoretical computer science, specifically using techniques from
      algebra to design algorithms.
    </p>

    <p>
      I have worked with <a class="link" href="http://users.cms.caltech.edu/~schulman/">Dr. Schulman</a> on identifying
      causal models, <a class="link" href="http://users.cms.caltech.edu/~umans/">Dr. Umans</a> on improving the
      bound on matrix multiplication, and <a class="link" href="https://ronnod.as/">Dr. Das</a> on
      counting arcs in projective planes.
    </p>

    <p>
      Other interests: tennis, film, and golf.
    </p>
  </div>

  <div class="leading-snug space-y-4">
    <p class="pb-2">Recent publications:</p>

    {#each featuredProjects as project}
      <a class="project-pair" href={project.href}>
        <div class="text-black font-medium">
          {project.name}
          <ArrowUpRight size={18} class="inline text-neutral-400" />
        </div>
        <div>
          <p>{project.desc}</p>
          {#if project.aside}
            <aside>{project.aside}</aside>
          {/if}
        </div>
      </a>
    {/each}
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
    @apply grid sm:grid-cols-[2fr,1fr] gap-y-1 -mx-3 px-3 py-2 hover:bg-neutral-100 transition-colors;
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
