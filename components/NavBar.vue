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
  </nav>
</template>
    
<script setup>
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

@media only screen and (max-width: 600px) {
  #nav-bar {
    display: none;
  }
}
</style>