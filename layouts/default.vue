<template>
  <div>
    <HamburgerMenu />
    <NavBar @routeChanged="handleClassChanged" :nameBar="currentClassName" />
    <slot />
  </div>
</template>

<script>
export default {
  mounted() {
    document.body.classList.add("gradient-body");
  },
  data() {
    return {
      currentClassName: "name-bar",
    };
  },
  methods: {
    handleClassChanged() {
      this.currentClassName = "name-bar active";
    },
  },
};
</script>


<style>
.gradient-body {
  background: linear-gradient(-45deg, #66fcf1, #46a29f, #202833);
  background-size: 400% 400%;
  animation: gradient 15s ease infinite;
  height: 100vh;
}

@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
</style>