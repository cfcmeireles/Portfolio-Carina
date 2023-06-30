<template>
  <div class="name-bar">
    <p style="font-size: 13px">Hire me</p>
    <p style="font-size: 13px">carinacmeireles@gmail.com</p>
    <NuxtLink to="https://github.com/cfcmeireles" target="_blank">
      <img
        src="../assets/github-logo.png"
        class="github-icon"
        alt="GitHub Logo"
      />
    </NuxtLink>
    <NuxtLink to="https://www.linkedin.com/in/carina-meireles/" target="_blank">
      <img
        src="../assets/linkedin-logo.png"
        class="linkedin-icon"
        alt="Linkedin Logo"
      />
    </NuxtLink>
  </div>
</template>
      
  <script>
export default {
  // data() {
  //   return {
  //     homeIsHovered: false,
  //     aboutMeIsHovered: false,
  //     ProjectsIsHovered: false,
  //     ContactsIsHovered: false,
  //   };
  // },
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
  position: fixed;
  bottom: 10px;
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