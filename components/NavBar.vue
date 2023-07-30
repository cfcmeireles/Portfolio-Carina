<template>
  <nav id="nav-bar">
    <ul class="nav-items">
      <div class="nav-item">
        <NuxtLink to="/" style="text-decoration: none; color: black">
          <li>HOME</li></NuxtLink
        >
        <div class="line"></div>
      </div>
      <div class="nav-item">
        <NuxtLink to="/aboutme" style="text-decoration: none; color: black"
          ><li>ABOUT</li></NuxtLink
        >
        <div class="line"></div>
      </div>
      <div class="nav-item">
        <NuxtLink to="/projects" style="text-decoration: none; color: black"
          ><li>PROJECTS</li></NuxtLink
        >
        <div class="line"></div>
      </div>
      <div class="nav-item">
        <NuxtLink to="/contacts" style="text-decoration: none; color: black"
          ><li>CONTACT</li></NuxtLink
        >
        <div class="line"></div>
      </div>
    </ul>
    <div :class="nameBar" v-if="showNameBar">
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
  </nav>
</template>
    
<script>
export default {
  props: {
    nameBar: {
      type: String,
    },
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
};
</script>
    
<style scoped>
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
  margin-bottom: 5px;
}

.nav-item {
  padding-bottom: 50px;
}

@media only screen and (max-width: 600px) {
  #nav-bar {
    display: none;
  }
}
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

.name-bar {
  opacity: 0;
  position: fixed;
  bottom: 10px;
  /* animation: fadeIn 1.5s ease-in-out; */
}

.name-bar.active {
  opacity: 1;
  animation: fadeIn 1.5s ease-in-out;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.github-icon {
  width: 3%;
}
.linkedin-icon {
  width: 3%;
}

/* .fade-enter-active {
  transition: opacity 1.5s ease-in-out;
}

.fade-enter-from {
  opacity: 0;
} */

@media only screen and (max-width: 600px) {
  #nav-bar {
    display: none;
  }
}
</style>