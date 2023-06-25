<template>
  <nav id="nav-bar">
    <ul class="nav-items">
      <div
        class="nav-item"
        @mouseover="homeIsHovered = true"
        @mouseleave="homeIsHovered = false"
      >
        <NuxtLink to="/" style="text-decoration: none; color: black">
          <li>Home</li></NuxtLink
        >
        <div
          class="horizontal-line"
          :class="{ 'move-right': homeIsHovered }"
        ></div>
      </div>
      <div
        class="nav-item"
        @mouseover="aboutMeIsHovered = true"
        @mouseleave="aboutMeIsHovered = false"
      >
        <NuxtLink to="/aboutme" style="text-decoration: none; color: black"
          ><li>About me</li></NuxtLink
        >
        <div
          class="horizontal-line"
          :class="{ 'move-right': aboutMeIsHovered }"
        ></div>
      </div>
      <div
        class="nav-item"
        @mouseover="ProjectsIsHovered = true"
        @mouseleave="ProjectsIsHovered = false"
      >
        <NuxtLink to="/projects" style="text-decoration: none; color: black"
          ><li>Projects</li></NuxtLink
        >
        <div
          class="horizontal-line"
          :class="{ 'move-right': ProjectsIsHovered }"
        ></div>
      </div>
      <div
        class="nav-item"
        @mouseover="ContactsIsHovered = true"
        @mouseleave="ContactsIsHovered = false"
      >
        <NuxtLink to="/contacts" style="text-decoration: none; color: black"
          ><li>Contacts</li></NuxtLink
        >
        <div
          class="horizontal-line"
          :class="{ 'move-right': ContactsIsHovered }"
        ></div>
      </div>
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
      homeIsHovered: false,
      aboutMeIsHovered: false,
      ProjectsIsHovered: false,
      ContactsIsHovered: false,
    };
  },
  mounted() {
    this.showNameBar = true;
  },
};
</script>
      
  <style scoped>
.move-right {
  transform: translateX(20px);
}
.horizontal-line {
  border-top: 1px black;
  transition: transform 0.3s ease-in-out;
}

.horizontal-line::before {
  content: "";
  display: block;
  border-top: 1px solid black;
}

.nav-items li {
  margin-bottom: 5px;
}

.nav-item {
  padding-bottom: 50px;
}

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

/* .nav-items li {
  padding-bottom: 50px;
} */

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