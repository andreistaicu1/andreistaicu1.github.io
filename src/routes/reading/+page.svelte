<script>
    const items = ['Meta-complexity', 'Error-Correcting Codes', 'Expanders', 'Quantum Cryptography', 'Differential Privacy'];
    const dates = ['9/18', '9/25', '10/2', '10/9', '10/16', '10/23', '10/30', '11/6', '11/13', '11/20', '12/4'];
</script>

<p
  class="layout-md text-black text-xl leading-tight font-light mb-2"
  id="UIUC_reading_group"
>

<article class="layout-lg">
  <img
    src={"/expander.png"}
    alt="Expander"
    class="float-right ml-6 mb-4 w-40 md:w-64 h-auto rounded-lg
           md:float-right float-none md:ml-6 ml-0" />

  <h1 class="text-3xl font-bold mb-6">Theory Reading Group</h1>
  <p class="text-lg mb-3">We intend to cover various topics in theoretical computer science, including but not limited to:</p>
  <ul class="list-disc list-outside pl-6 space-y-1">
    {#each items as item}
        <li>{item}</li>
    {/each}
  </ul>
  <div class="clear-both"></div>
</article>

<p class="layout-lg text-lg mt-2 mb-6">The reading group is led by <a class="link" href="https://granha.github.io/">Prof. Fernando Granha Jeronimo</a> 
    with help from student organizers Will, <a class="link" href="/">Andrei</a>, and Rhea. We will meet in SC 3102 on Thursdays from 5-8PM, 
    starting on September 18th.</p>

<hr />

<h2 class="text-2xl font-bold mb-6 mt-6">Schedule:</h2>

