<script lang="ts">
  import "@fontsource/newsreader/400-italic.css";
  import "../../app.css";
</script>

<div class="min-h-dvh bg-white text-slate-900 dark:bg-slate-950 dark:text-slate-100">
  <header class="border-b bg-orange-50">
    <nav class="layout-md flex items-center gap-6 py-4">
      <a href="/reading" class="font-semibold text-2xl">Fall 2025</a>
      <a href="/" class="link ml-auto">Home</a>
    </nav>
  </header>

  <main class="layout-md py-8">
    <!-- your pages render here -->
    <slot />
  </main>

  <footer class="border-t bg-blue-50">
    <div class="layout-md py-6 text-lg text-slate-500">
      <a href="https://theoryincs.web.illinois.edu/" class="link">UIUC TCS</a>
    </div>
  </footer>
</div>

