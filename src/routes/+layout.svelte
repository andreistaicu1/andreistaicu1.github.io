<script lang="ts">
  import "@fontsource/newsreader/400-italic.css";
  import "../app.css";

  import { browser, dev } from "$app/environment";
  import { page } from "$app/stores";

  import { fly } from "svelte/transition";

  import Header from "$lib/components/Header.svelte";
  import Footer from "$lib/components/Footer.svelte";
  import type { LayoutData } from "./$types";

  export let data: LayoutData;

  const isMobile = browser && /Android|iPhone/i.test(navigator.userAgent);
  const reducedMotion =
    browser && matchMedia("(prefers-reduced-motion: reduce)").matches;

  const HIDE_ON: RegExp[] = [
    /^\/reading(\/|$)/
  ];
  $: hideHeader =
    HIDE_ON.some((re) => re.test($page.url.pathname)) ||
    (browser && $page.url.searchParams.get("noheader") === "1"); // only access searchParams in browser
</script>

<svelte:head>
  <!-- Global site tag (gtag.js) - Google Analytics -->
  {#if !dev}
    <script
      async
      src="https://www.googletagmanager.com/gtag/js?id=UA-156644599-1"
    ></script>
    <script>
      window.dataLayer = window.dataLayer || [];
      function gtag() {
        dataLayer.push(arguments);
      }
      gtag("js", new Date());
      gtag("config", "UA-156644599-1");
    </script>
  {/if}
</svelte:head>

{#if !hideHeader}
  <Header />
{/if}


{#if isMobile || reducedMotion}
  <!--
    Disable page transitions on mobile due to a browser engine bug.
    Also disable them for reduced-motion users.
  -->
  <main>
    <slot />
  </main>
{:else}
  {#key data.pathname}
    <main
      in:fly={{ x: -10, duration: 350, delay: 350 }}
      out:fly={{ y: 5, duration: 350 }}
    >
      <slot />
    </main>
  {/key}
{/if}

<Footer />
