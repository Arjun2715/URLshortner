<template>
  <div class="navbar bg-base-200">
    <div class="navbar-start">
      <div class="dropdown">
        <label tabindex="0" class="btn btn-ghost lg:hidden">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-5 w-5"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h8m-8 6h16"
            />
          </svg>
        </label>
        <ul
          tabindex="0"
          class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52"
        >
          <li><a :href="githubLink" target="_blank">Github</a></li>
          <li>
            <a :href="linkedinLink" target="_blank">LinkedIn</a>
          </li>
        </ul>
      </div>
      <a class="btn btn-ghost normal-case text-xl">Url Shortner</a>
    </div>
    <div class="navbar-center hidden lg:flex">
      <ul class="menu menu-horizontal px-1">
        <li><a :href="githubLink" target="_blank">Github</a></li>
        <li><a :href="linkedinLink" target="_blank">LinkedIn</a></li>
      </ul>
    </div>
    <div class="navbar-end">
      <a class="btn">Button</a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      githubLink: "https://github.com/Arjun2715",
      linkedinLink: "https://www.linkedin.com/in/arjunjot-singh",
    };
  },
};
</script>

<style>
</style>