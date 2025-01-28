<script lang="ts">
    import { fade } from "svelte/transition";
    import Markdown from "$lib/components/Markdown.svelte";
    import { formatTime } from "$lib/utils";
  
    type Paper = {
      title: string;
      date: string;
      content: string;
      topics: string[];
      authors: string;
      publication: string;
    }

    export let data: Paper;

  let isCollapsed = true;

  function toggleCollapse() {
    isCollapsed = !isCollapsed;
  }
</script>

  <!-- Title -->
<h3 class="text-black text-xl font-semibold mb-1">
  <span class="mr-1">{data.title}</span>
  <small class="whitespace-nowrap text-black-500 text-base font-normal italic">
    {data.publication}
  </small>
  <small class="whitespace-nowrap text-neutral-500 text-base font-normal">
    {formatTime("%B %Y", data.date)}
  </small>
</h3>

<!-- Authors -->
<div class="text-neutral-600 text-md font-light mb-2">
  <span class="text-md font-light mb-3">{data.authors}</span>
</div>

<!-- Description and Tags -->
<div class="space-y-4">
  <div class="w-full flex items-center space-x-4">
    <!-- Collapse Button -->
    <button
      on:click={toggleCollapse}
      class="text-blue-500 hover:underline"
    >
      {isCollapsed ? "Show Abstract" : "Hide Abstract"}
    </button>

    <!-- Tags (Pill Bar) -->
    <div class="flex flex-wrap space-x-2">
      {#each data.topics as tag}
        <div class="pill">{tag}</div>
      {/each}
    </div>
  </div>

  <!-- Collapsible Content -->
  {#if !isCollapsed}
    <div class="markdown-content">
      <Markdown source={data.content} />
    </div>
  {/if}
</div>

<style lang="postcss">
  .pill {
    @apply flex items-center text-sm font-medium;
    @apply px-1.5 py-[1px] mr-1.5 mb-2 bg-neutral-100 rounded-full;
  }
</style>
