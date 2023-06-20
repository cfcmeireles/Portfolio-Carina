<template>
  <NavBar />
  <transition name="fade">
    <div class="name-bar" v-if="showNameBar">
      <p style="font-size: 13px">Hire me</p>
      <p style="font-size: 13px">carinacmeireles@gmail.com</p>
      <NuxtLink to="https://github.com/cfcmeireles" target="_blank">
        <img
          src="../assets/github-logo.png"
          class="github-icon"
          alt="GitHub Logo"
        />
      </NuxtLink>
      <NuxtLink
        to="https://www.linkedin.com/in/carina-meireles/"
        target="_blank"
      >
        <img
          src="../assets/linkedin-logo.png"
          class="linkedin-icon"
          alt="Linkedin Logo"
        />
      </NuxtLink>
    </div>
  </transition>
</template>
      
  <script>
export default {
  data() {
    return {
      showNameBar: false,
    };
  },
  mounted() {
    this.showNameBar = true;
  },
};
</script>
      
  <style scoped>
/* .nav-items li {
  padding-bottom: 50px;
} */
.name-bar {
  position: absolute;
  bottom: 0;
}

.github-icon {
  width: 3%;
}
.linkedin-icon {
  width: 3%;
}

.fade-enter-active {
  transition: opacity 1.5s ease-in-out;
}

.fade-enter-from {
  opacity: 0;
}

@media only screen and (max-width: 600px) {
  #nav-bar {
    display: none;
  }
}
</style>