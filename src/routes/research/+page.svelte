<script lang="ts">
    import { page } from "$app/stores";
    import { onMount } from "svelte";

    import Seo from "$lib/components/Seo.svelte";
    import Paper from "./Research.svelte";

    const papers = import.meta.glob("../../papers/*.md", {
        eager: true,
    }) as any;

    $: papersByDate = Object.keys(papers).sort(
        (a, b) => papers[b].date - papers[a].date
    );

    function trimName(id: string) {
        return id.match(/\.\.\/projects\/(.*)\.md$/)?.[1];
    }

    let sortOrder: "date" | "other" = "date";
</script>
  
<Seo
title="Andrei Staicu – Research"
description="Publications."
/>

<section class="layout-md py-8">
    <h2 class="heading2">Recent Publications</h2>
{#each papersByDate as id (id)}
    <div class="mx-auto max-w-[1152px] px-4 sm:px-6 py-4">
      <Paper data={papers[id]} />
    </div>
{/each}
</section>

<style lang="postcss">
  button {
    @apply flex items-center text-neutral-400 transition-colors hover:text-black;
  }

  button.active {
    @apply text-black;
  }
</style>
