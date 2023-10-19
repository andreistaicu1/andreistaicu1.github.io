<footer class="layout-md mt-20 text-lg flex flex-col">
  <div class="row">
    <span>GitHub</span>
    <hr />
    <a class="link" href="https://github.com/andreistaicu1">@andreistaicu1</a>
  </div>
  <div class="row">
    <span>Email</span>
    <hr />
    <a class="link" href="mailto:andreistaicu01@gmail.com">andreistaicu01@gmail.com</a>
  </div>
  <div class="row">
    <span>Linkedin</span>
    <hr />
    <a class="link" href="https://www.linkedin.com/in/andrei-staicu-4ba3b9202/">Andrei Staicu</a>
  </div>
  <div class="row">
    <span>Website Credits</span>
    <hr />
    <a class="link" href="https://www.ekzhang.com/">Eric Zhang</a>
  </div>
</footer>

<style lang="postcss">
  .row {
    @apply flex items-center space-x-4;
    max-width: 100%; /* Set a maximum width for each row */
    white-space: nowrap;
  }

  .row span {
    @apply text-neutral-500;
  }

  .row hr {
    @apply w-full mt-0.5 border-neutral-300 border-dotted;
  }
</style>
