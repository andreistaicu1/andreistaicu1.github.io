<script lang="ts">
  import Seo from "$lib/components/Seo.svelte";
  import Workplace from "./Workplace.svelte";
</script>

<Seo
  title="Andrei Staicu – Resume"
  description="Theoretical computer scientist."
/>

<section class="layout-md py-8">
  <h2 class="heading2">Honors and Awards</h2>
    <h4 class="font-light mt-1 mb-0"><em><a class="link" href="https://www.cms.caltech.edu/academics/honors"
      >Bhansali Family Prize in Computer Science</a></em> - 2024</h4>
    <h4 class="font-light mt-1 mb-0"><em>
      Caltech Summer Undergraduate Research Fellow</em> - 2021, 2022, and 2023</h4>
    <h4 class="font-light mt-1 mb-0"><em><a class="link" href="https://pma.caltech.edu/research-and-academics/mathematics/prizes-and-awards-in-mathematics/apostol-award-for-excellence-in-teaching-in-mathematics-winners"
      >Apostol Award for Excellence in Teaching in Mathematics</a></em> - 2023</h4>
</section>

<section class="layout-md py-4">
  <h2 class="heading2">Projects</h2>
    <h3 class="text-black text-lg leading-tight mb-1">Finite Field Linear Algebra Library</h3>
    <p class="font-light mb-2">
    <span class="whitespace-nowrap"><a class="link" href="https://github.com/andreistaicu1/FieldLinAlg.git">src</a></span>
    <span class="px-0.5 text-neutral-500">•</span>
    <span class="whitespace-nowrap">C++</span>
    <span class="px-0.5 text-neutral-500">•</span>
    <span class="whitespace-nowrap">with <a class="link" href="https://github.com/ericluap">@ericluap</a></span>
  </p>
</section>

<section class="layout-md py-4">
  <h2 class="heading2">Contact</h2>
    <h4 class="font-light mt-1 mb-1">LinkedIn: <a class="link" href="https://www.linkedin.com/in/andrei-staicu-4ba3b9202/">Andrei Staicu</a></h4>
    <h4 class="font-light mt-1 mb-1">GitHub: <a class="link" href="https://github.com/andreistaicu1">@andreistaicu1</a></h4>
    <h4 class="font-light mt-1 mb-1">Email: <span class="font-mono bg-gray-200 px-1 py-0.5 rounded">[first-initial][last]2[at]illinois.edu/span></h4>
</section>


<style lang="postcss">
  b {
    @apply font-medium;
  }

  ul {
    @apply list-disc pl-7 marker:text-neutral-400;
  }

  .byline {
    @apply font-serif italic;
  }
</style>
