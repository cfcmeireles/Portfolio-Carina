<template>
  <nav
    class="hidden md:fixed md:left-0 md:h-full lg:block lg:fixed lg:left-0 lg:h-full"
  >
    <ul class="pl-10 my-4 list-none h-full flex justify-center flex-col">
      <div class="nav-item pb-12">
        <NuxtLink to="/" style="text-decoration: none; color: black">
          <li class="mb-1.5 font-mono text-white text-xs">HOME</li></NuxtLink
        >
        <div class="line"></div>
      </div>
      <div class="nav-item pb-12">
        <NuxtLink to="/aboutme" style="text-decoration: none; color: black"
          ><li class="mb-1.5 font-mono text-white text-xs">ABOUT</li></NuxtLink
        >
        <div class="line"></div>
      </div>
      <div class="nav-item pb-12">
        <NuxtLink to="/projects" style="text-decoration: none; color: black"
          ><li class="mb-1.5 font-mono text-white text-xs">
            PROJECTS
          </li></NuxtLink
        >
        <div class="line"></div>
      </div>
      <div class="nav-item pb-12">
        <NuxtLink to="/contact" style="text-decoration: none; color: black"
          ><li class="mb-1.5 font-mono text-white text-xs">
            CONTACT
          </li></NuxtLink
        >
        <div class="line"></div>
      </div>
    </ul>
    <div
      :class="[showWithFade ? 'name-bar active' : 'name-bar']"
      class="pl-5"
      v-if="showNameBar"
    >
      <NuxtLink to="https://github.com/cfcmeireles" target="_blank">
        <img
          src="../assets/github-icon.svg"
          class="w-8 mr-2"
          alt="GitHub Logo"
        />
      </NuxtLink>
      <NuxtLink
        to="https://www.linkedin.com/in/carina-meireles/"
        target="_blank"
      >
        <img
          src="../assets/linkedin-icon.svg"
          class="w-8"
          alt="Linkedin Logo"
        />
      </NuxtLink>
    </div>
  </nav>
</template>
    
<script>
export default {
  props: {
    showWithFade: Boolean,
    showNameBar: {
      type: Boolean,
      required: true,
    },
  },
  watch: {
    $route() {
      this.$emit("routeChanged");
    },
  },
  data() {
    return {
      showWithFade: true,
    };
  },
};
</script>
    
<style scoped>
@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.name-bar {
  opacity: 0;
  position: fixed;
  bottom: 10px;
}

.name-bar.active {
  opacity: 1;
  animation: fadeIn 1.5s ease-in-out;
}

.nav-item:hover .line {
  transform: translateX(20px);
}

.line {
  transition: transform 0.3s ease-in-out;
}

.line::before {
  content: "";
  display: block;
  border-top: 1px solid #66fcf1;
}
</style>