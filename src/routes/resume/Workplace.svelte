<script lang="ts">
  import { fade } from "svelte/transition";

  export let title: string;
  export let company: string;
  export let dates: string;
  export let location: string;
  export let prof: string;
  export let defaultHidden = false;

  let hidden = defaultHidden;
</script>

<div
  class="mb-8"
  class:cursor-pointer={hidden}
  on:click={() => (hidden = false)}
  on:keypress={() => {}}
>
  <h3 class="text-black text-lg leading-tight mb-1">
    {title} at {company}
  </h3>
  <p class="font-light mb-2">
    <span class="whitespace-nowrap">{dates}</span>
    <span class="px-0.5 text-neutral-500">•</span>
    <span class="whitespace-nowrap">{location}</span>
    <span class="px-0.5 text-neutral-500">•</span>
    <span class="whitespace-nowrap">{prof}</span>
  </p>
  {#if !hidden}
    <ul class="list-disc pl-7 marker:text-neutral-400" in:fade|local>
      <slot />
    </ul>
  {/if}
</div>
