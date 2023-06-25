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
  </nav>
</template>
    
<script>
export default {
  data() {
    return {
      homeIsHovered: false,
      aboutMeIsHovered: false,
      ProjectsIsHovered: false,
      ContactsIsHovered: false,
    };
  },
};
</script>
    
<style>
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