<template>
  <div class="top-menu block w-full h-16 m-0 fixed top-0 left-0 lg:hidden z-50">
    <nav
      class="hamburger-menu block absolute top-5"
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

      <ul class="nav-items hidden h-64 top-4 text-center font-rubik">
        <NuxtLink to="/" style="text-decoration: none"> <li>Home</li></NuxtLink>
        <NuxtLink to="/aboutme" style="text-decoration: none"
          ><li>About me</li></NuxtLink
        >
        <NuxtLink to="/projects" style="text-decoration: none"
          ><li>Projects</li></NuxtLink
        >
        <NuxtLink to="/contacts" style="text-decoration: none"
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
  display: flex;
  justify-content: center;
  align-items: center;
  height: 25%;
}

.top-menu {
  background-color: lightblue;
}
.hamburger-menu ul {
  background-color: lightblue;
}

.hamburger-menu ul li {
  opacity: 1;
}
</style>