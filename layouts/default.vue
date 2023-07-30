<template>
  <div>
    <HamburgerMenu />
    <NavBar
      @routeChanged="handleClassChanged"
      :nameBar="currentClassName"
      :showNameBar="showNameBar"
    />
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
      showNameBar: true,
    };
  },
  methods: {
    handleClassChanged() {
      if (this.$route.path !== "/") {
        (this.showNameBar = false),
          setTimeout(() => {
            this.currentClassName = "name-bar active";
            this.showNameBar = true;
          }, 1000);
      } else {
        this.showNameBar = false;
        this.currentClassName = "name-bar";
      }
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