<script lang="ts">
  import Seo from "$lib/components/Seo.svelte";
  import Workplace from "./Workplace.svelte";
</script>

<Seo
  title="Andrei Staicu – Resume"
  description="Theoretical computer scientist."
/>

<section class="layout-md py-12">
  <h2 class="heading2">Education</h2>

  <div class="mb-4">
    <div class="flex justify-between items-end">
      <h3 class="text-black text-lg">California Institute of Technology</h3>
      <div class="text-neutral-500 mb-0.5">2020 —</div>
    </div>
    <p class="byline">B.S. in Mathemtatics</p>
  </div>

  <h4 class="font-medium mt-4 mb-1">Teaching:</h4>
  <ul>
    <li>
      TA for Introduction to Abstract Algebra (Ma 5b), Winter 2023
    </li>
  </ul>

  <h4 class="font-medium mt-4 mb-1">Graduate-level technical coursework:</h4>
  <ul>
    <li>Algebraic Geometry (Ma 130ab)</li>
    <li>Commutative Algebra (Ma 120a)</li>
    <li>Complexity Theory (CS 151)</li>
    <li>Computability Theory (Ma/CS 117ab)</li>
    <li>Discrete Differential Geometry: Theory and Applications (CS/ACM 177a)</li>
  </ul>

  <h4 class="font-medium mt-4 mb-1">Undergraduate technical coursework:</h4>
  <ul>
    <li>Introduction to Abstract Algebra (Ma 5abc)</li>
    <li>Introduction to Geometry and Topology (Ma 109abc)</li>
    <li>Classical Analysis (Ma 108abc)</li>
    <li>Algorithms (CS 38)</li>
    <li>Introduction to Discrete Mathematics (Ma 6a)</li>
    <li>Learning Systems (CS 156a)</li>
    <li>Introduction to Computing Systems (CS 24)</li>
    <li>Decidability and Tractability (CS 21)</li>
  </ul>
</section>

<section class="layout-md py-12">
  <h2 class="heading2">Research</h2>

  <Workplace
    title="Theoretical Computer Science Researcher"
    company="Caltech"
    dates="January 2023 – Current"
    location="Pasadena, CA"
    prof="mentored by Prof. Leonard Schulman"
  >
    <li>
      Established foundation in computational algebraic geometry, representation theory, and invariant theory
    </li>
    <li>
      Led weekly research group meetings and wrote code in Mathematica and SageMath to make informed conjectures
    </li>
    <li>
      Co-authored paper: proved the main identifiability result and wrote up my contribution, Theorem 17
    </li>
  </Workplace>

  <Workplace
    title="Theoretical Computer Science Researcher"
    company="Caltech"
    dates="September 2022 - September 2023"
    location="Pasadena, CA"
    prof="mentored by Prof. Chris Umans"
  >
    <li>
      Read and presented recent advancements in bounds for group theoretic matrix multiplication algorithms
    </li>
    <li>
      Held weekly meeetings and wrote code in SageMath that tested the standard constructions to make conjectures
    </li>
  </Workplace>

  <Workplace
    title="Mathematics Researcher"
    company="the University of Copenhagen"
    dates="June 2022 – October 2022"
    location="Copenhagen, Denmark"
    prof="mentored by Dr. Ronno Das"
  >
    <li>
      Computed all the counts for 7-arcs in char 2 and a majority of twisted 8-arcs in odd char, all are novel results
    </li>
    <li>
      Presented results to the Dept Math, U Copenhagen and the Caltech SURF Seminar Day 2022
    </li>
  </Workplace>
</section>

<section class="layout-md py-4">
  <h2 class="heading2">Publications</h2>
    <h4 class="font-light mt-4 mb-1">Gordon, S., Kant, M., Ma, E., Schulman, L.J., and <b>Staicu, A.</b> (2023). 
      “Identifiability of Product of Experts Models” arXiv preprint <a class="link" 
      href="https://arxiv.org/abs/2310.09397?context=math.AG">arXiv:2310.09397</a>.</h4>
    <h4 class="font-light mt-4 mb-1"><b>Staicu, A.</b> (2023). 
      “Counting 7-Arcs in Projective Planes over Finite Fields” arXiv preprint <a class="link" 
      href="https://arxiv.org/abs/2311.16578">arXiv:2311.16578</a>.</h4>
</section>

<section class="layout-md py-4">
  <h2 class="heading2">Honors and Awards</h2>
    <h4 class="font-light mt-4 mb-1"><em><a class="link" href="https://pma.caltech.edu/research-and-academics/mathematics/prizes-and-awards-in-mathematics/apostol-award-for-excellence-in-teaching-in-mathematics-winners"
      >Apostol Award for Excellence in Teaching in Mathematics</a></em> - Introduction to Abstract Algebra (Ma 5b), 
      Winter 2023</h4>
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
    <ul>
      <li>
        Built representation of finite fields using polynomials and numerical methods from
        <a class="link" href="https://link.springer.com/book/10.1007/978-3-662-02945-9">
          Computational Number Theory</a> by Henri Cohen.
      </li>
      <li>
        Implemented the probabalistic method for calculating irrreducible polynomials of arbitrary
        degree over finite fields of order prime.
      </li>
    </ul>
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
