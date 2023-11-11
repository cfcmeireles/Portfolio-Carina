<template>
  <body class="bg-darkblue">
    <nav
      class="hidden md:block md:fixed md:left-0 md:h-full lg:block lg:fixed lg:left-0 lg:h-full"
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
            ><li class="mb-1.5 font-mono text-white text-xs">
              ABOUT
            </li></NuxtLink
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
          <NuxtLink to="/contacts" style="text-decoration: none; color: black"
            ><li class="mb-1.5 font-mono text-white text-xs">
              CONTACT
            </li></NuxtLink
          >
          <div class="line"></div>
        </div>
      </ul>
      <div
        :class="[showWithFade ? 'name-bar active' : 'name-bar']"
        v-if="showNameBar"
      >
        <p style="font-size: 13px">Hire me</p>
        <p style="font-size: 13px">carinacmeireles@gmail.com</p>
        <NuxtLink to="https://github.com/cfcmeireles" target="_blank">
          <img src="../assets/github-logo.png" class="w-8" alt="GitHub Logo" />
        </NuxtLink>
        <NuxtLink
          to="https://www.linkedin.com/in/carina-meireles/"
          target="_blank"
        >
          <img
            src="../assets/linkedin-logo.png"
            class="w-8"
            alt="Linkedin Logo"
          />
        </NuxtLink>
      </div>
    </nav>
  </body>
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
  border-top: 1px #66fcf1;
  transition: transform 0.3s ease-in-out;
}

.line::before {
  content: "";
  display: block;
  border-top: 1px solid black;
}
</style>