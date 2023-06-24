<template>
  <nav id="nav-bar">
    <ul class="nav-items">
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
  </nav>
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
#nav-bar {
  position: fixed;
  left: 0;
  height: 100%;
}
.nav-items {
  list-style: none;
  height: 100%;
  display: flex;
  justify-content: center;
  flex-flow: column;
}

.nav-items li {
  padding-bottom: 50px;
}

@media only screen and (max-width: 600px) {
  #nav-bar {
    display: none;
  }
}
/* .nav-items li {
  padding-bottom: 50px;
} */
.name-bar {
  position: absolute;
  bottom: 10px;
}

.github-icon {
  width: 20%;
}
.linkedin-icon {
  width: 20%;
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