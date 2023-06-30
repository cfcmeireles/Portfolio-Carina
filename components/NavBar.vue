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
  </nav>
</template>
    
<script>
// export default {
//   data() {
//     return {
//       clicked: false,
//       homeIsHovered: false,
//       aboutMeIsHovered: false,
//       ProjectsIsHovered: false,
//       ContactsIsHovered: false,
//     };
//   },
// };
</script>
    
<style>
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
</style>