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
</style>