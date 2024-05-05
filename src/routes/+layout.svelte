<script>
    import "../app.css";
    import { onMount } from 'svelte'
    import { themeChange } from 'theme-change'

    // NOTE: the element that is using one of the theme attributes must be in the DOM on mount
    onMount(() => {
      themeChange(false)
      // 👆 false parameter is required for svelte
    })
</script>

<div class="navbar bg-base-100">
  <div class="flex-none">
    <div class="dropdown">
      <button class="btn btn-square btn-ghost">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" class="inline-block w-5 h-5 stroke-current"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path></svg>
      </button>
      <ul tabindex="0" class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52">
        <li><a href="/">Home</a></li>
        <li><a href="/">About</a></li>
      </ul>
    </div>
  </div>

  <div class="flex-1">
    <a href="/" class="btn btn-ghost text-xl">rosecube</a>
  </div>

  <div class="flex-none mr-2">
    <!-- Theme changer -->
    <label class="flex cursor-pointer gap-2">
      <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="5"/><path d="M12 1v2M12 21v2M4.2 4.2l1.4 1.4M18.4 18.4l1.4 1.4M1 12h2M21 12h2M4.2 19.8l1.4-1.4M18.4 5.6l1.4-1.4"/></svg>
      <input type="checkbox" value="lemonade" class="toggle theme-controller"/>
      <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"></path></svg>
    </label>
  </div>
</div>


<slot />
