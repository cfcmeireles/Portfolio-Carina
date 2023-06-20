<template>
  <nav id="nav-bar">
    <ul class="nav-items">
      <NuxtLink to="/" style="text-decoration: none; color: black">
        <li>
          <img src="../assets/home-icon.png" class="home-icon" /> Home
        </li></NuxtLink
      >
      <NuxtLink to="/aboutme" style="text-decoration: none; color: black"
        ><li>
          <img src="../assets/aboutme-icon.png" class="aboutme-icon" /> About me
        </li></NuxtLink
      >
      <NuxtLink to="/projects" style="text-decoration: none; color: black"
        ><li>
          <img src="../assets/projects-icon.png" class="projects-icon" />
          Projects
        </li></NuxtLink
      >
      <NuxtLink to="/contacts" style="text-decoration: none; color: black"
        ><li>
          <img src="../assets/email-icon.png" class="contacts-icon" /> Contacts
        </li></NuxtLink
      >
    </ul>
    <transition name="fade">
      <div class="name-bar" v-if="showNameBar">
        <p>Carina Meireles</p>
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
    // Set showElement to true after component is mounted to trigger the fade-in animation
    this.showNameBar = true;
  },
};
</script>
      
  <style scoped>
#nav-bar {
  position: fixed;
  left: 0;
  height: 100%;
  top: -20px;
}
.nav-items {
  list-style: none;
  background-color: white;
  height: 100%;
  width: 150%;
  padding-top: 200%;
}

.nav-items li {
  padding-bottom: 50px;
}

.home-icon,
.aboutme-icon,
.projects-icon,
.contacts-icon {
  width: 13%;
  height: 25px;
}

.name-bar {
  position: absolute;
  bottom: 0;
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