<template>
  <div class="hamburger-bar">
    <nav
      class="hamburger-menu"
      @click="toggleMenu"
      :class="isActive ? 'active' : ''"
    >
      <span class="bar"></span>
      <span class="bar"></span>
      <span class="bar"></span>

      <ul class="nav-items">
        <NuxtLink to="/" style="text-decoration: none; color: black">
          <li>
            <img src="../assets/home-icon.png" class="home-icon" /> Home
          </li></NuxtLink
        >
        <NuxtLink to="/aboutme" style="text-decoration: none; color: black"
          ><li>
            <img src="../assets/aboutme-icon.png" class="aboutme-icon" /> About
            me
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
            <img src="../assets/email-icon.png" class="projects-icon" />
            Contacts
          </li></NuxtLink
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
* {
  background-color: #333;
}
.hamburger-bar {
  display: none;
}

.hamburger-menu {
  display: none;
}

.bar {
  position: relative;
  display: block;
  width: 25px;
  height: 3px;
  margin: 5px 0;
  transition: all 0.3s ease;
  background-color: white;
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

.nav-items {
  display: none;
}

.hamburger-menu.active .nav-items {
  display: block;
  position: absolute;
  left: -30px;
  width: 100px;
}
.hamburger-menu.active .nav-items li {
  color: white;
  list-style: none;
}

.home-icon,
.aboutme-icon,
.projects-icon {
  width: 23%;
  height: 25px;
}

@media only screen and (max-width: 950px) {
  .hamburger-menu {
    display: block;
    position: absolute;
    top: 20px;
    left: 15px;
  }
  .hamburger-bar {
    display: block;
    background-color: #333;
    width: 100%;
    height: 70px;
    margin: 0;
    position: absolute;
    top: 0;
    left: 0;
  }
}
</style>