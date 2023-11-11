<template>
  <div
    class="bg-gray-500 block w-full h-16 m-0 absolute top-0 left-0 md:hidden lg:hidden"
  >
    <nav
      class="hamburger-menu bg-gray-500 block absolute top-5"
      @click="toggleMenu"
      :class="isActive ? 'active' : ''"
    >
      <span
        class="bar relative block w-6 h-1 my-1 mx-0 bg-white transition-all duration-300 ease-in"
      ></span>
      <span
        class="bar relative block w-6 h-1 my-1 mx-0 bg-white transition-all duration-300 ease-in"
      ></span>
      <span
        class="bar relative block w-6 h-1 my-1 mx-0 bg-white transition-all duration-300 ease-in"
      ></span>

      <ul class="nav-items hidden bg-gray-500 text-center font-rubik">
        <NuxtLink to="/" style="text-decoration: none; color: black">
          <li>Home</li></NuxtLink
        >
        <NuxtLink to="/aboutme" style="text-decoration: none; color: black"
          ><li>About me</li></NuxtLink
        >
        <NuxtLink to="/projects" style="text-decoration: none; color: black"
          ><li>Projects</li></NuxtLink
        >
        <NuxtLink to="/contacts" style="text-decoration: none; color: black"
          ><li>Contacts</li></NuxtLink
        >
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isActive = !this.isActive;
    },
  },
};
</script>

<style scoped>
.hamburger-menu {
  left: 5px;
}

.nav-items {
  position: relative;
  left: -5px;
}
.hamburger-menu.active .bar:nth-child(1) {
  transform: translateY(8px) rotate(45deg);
}

.hamburger-menu.active .bar:nth-child(2) {
  opacity: 0;
}

.hamburger-menu.active .bar:nth-child(3) {
  transform: translateY(-8px) rotate(-45deg);
}

.hamburger-menu.active .nav-items {
  display: block;
}

.hamburger-menu.active .nav-items li {
  color: white;
  list-style: none;
  width: 100vw;
}
</style>