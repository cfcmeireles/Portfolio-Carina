<template>
  <div
    class="hamburger-menu block w-full h-16 m-0 absolute top-2 lg:hidden z-50"
    :class="isActive ? 'active' : ''"
    @click="toggleMenu"
    @click.stop
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

    <ul class="nav-items hidden h-80 bottom-9 text-center font-rubik pt-10">
      <NuxtLink to="/" style="text-decoration: none"> <li>Home</li></NuxtLink>
      <NuxtLink to="/aboutme" style="text-decoration: none"
        ><li>About me</li></NuxtLink
      >
      <NuxtLink to="/projects" style="text-decoration: none"
        ><li>Projects</li></NuxtLink
      >
      <NuxtLink to="/contact" style="text-decoration: none"
        ><li>Contact</li></NuxtLink
      >
    </ul>
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
    closeMenuOnPageClick(e) {
      if (!e.target.classList.contains("active")) {
        this.isActive = false;
      }
    },
  },
  mounted() {
    document.body.addEventListener("click", this.closeMenuOnPageClick);
  },
  beforeDestroy() {
    document.body.removeEventListener("click", this.closeMenuOnPageClick);
  },
};
</script>

<style scoped>
.bar {
  z-index: 99;
}
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
  color: #202833;
  list-style: none;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 25%;
}

.hamburger-menu.active {
  animation: fadeIn 0.5s ease-in-out;
}

.hamburger-menu.active .bar {
  background: #202833;
}
.hamburger-menu ul {
  background-color: lightblue;
}
.hamburger-menu ul li {
  opacity: 1;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
