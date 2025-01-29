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
  <div class="grid grid-cols-[4fr_1fr] gap-4 items-left">
    <div class="text-left">
      <h3 class="text-black text-lg font-semibold inline">
        <span>{data.title}</span>
      </h3>
      <small class="whitespace-nowrap text-black-500 text-base font-normal italic ml-2">
        {data.publication}
      </small>
    </div>
    <!-- Date -->
    <small class="whitespace-nowrap text-neutral-500 text-base font-normal text-right">
      {formatTime("%B %Y", data.date)}
    </small>
  </div>


<!-- Description and Tags -->
<div class="space-y-4">
  <div class="w-full flex items-center space-x-2">
    <!-- Collapse Button -->
    <button
      on:click={toggleCollapse}
      class="text-blue-500 hover:underline font-mono"
    >
      {isCollapsed ? "[+]" : "[-]"}
    </button>

    <!-- Authors -->
    <div class="text-neutral-600 text-md font-light">
      <span class="text-md font-light mb-2">{data.authors}</span>
    </div>
  </div>

  <!-- Collapsible Content -->
  {#if !isCollapsed}
    <div class="markdown-content px-4 mb-2">
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
