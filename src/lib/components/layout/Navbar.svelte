<script lang="ts">
  import ThemeToggle from "./../ui/ThemeToggle.svelte";
  import Helper from "./../ui/Helper.svelte";
  let Webname = "Arth Panel";

  type NavType = "default" | "welcome";

  export let navType: NavType;
</script>

{#if navType === "default"}
  <div class="navbar bg-base-300 px-4">
    <div class="flex-1">
      <a class="btn btn-ghost normal-case text-xl invisible sm:visible" href="/"
        ><img src="/images/sitelogo.svg" alt="Arth" width="75" height="75" /></a
      >
    </div>
    <div class="flex-none space-x-2">
      <ul class="menu menu-horizontal p-0">
        <li><a href="/">Home</a></li>
        <li><a href="/hosting">Hosting</a></li>
      </ul>

      <ThemeToggle />

      <div class="dropdown dropdown-end">
        <label tabindex="0" class="btn btn-ghost btn-circle">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="feather feather-menu"
            ><line x1="3" y1="12" x2="21" y2="12" /><line
              x1="3"
              y1="6"
              x2="21"
              y2="6"
            /><line x1="3" y1="18" x2="21" y2="18" /></svg
          ><path
            d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"
          /><path
            d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"
          />
        </label>
        <ul
          tabindex="0"
          class="mt-3 p-2 shadow menu menu-compact dropdown-content bg-base-200 rounded-box w-52"
        >
          <li>
            <a
              href="https://discord.com/invite/bjY39AbK35"
              class="justify-between"
            >
              Discord
            </a>
          </li>
          <li>
            <a href="/software" class="justify-between"> Software </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
{:else if navType === "welcome"}
  <div class="navbar fixed justify-between px-6">
    <a class="btn btn-ghost normal-case text-2xl" href="/">{Webname}</a>
    <ThemeToggle />
  </div>
{/if}
