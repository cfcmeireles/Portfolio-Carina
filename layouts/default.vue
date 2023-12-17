<template>
  <div class="layout">
    <div class="nav-bars">
      <HamburgerMenu />
      <NavBar @routeChanged="handleClassChanged" :showNameBar="showNameBar" />
    </div>
    <div>
      <slot />
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    this.handleClassChanged();
  },
  data() {
    return {
      timeOut: null,
      showNameBar: true,
    };
  },
  methods: {
    handleClassChanged() {
      const timeOutFunction = () => {
        this.showNameBar = true;
      };
      if (this.$route.path !== "/") {
        (this.showNameBar = false),
          (this.timeOut = setTimeout(timeOutFunction, 1000));
      } else {
        clearTimeout(this.timeOut);
        this.showNameBar = false;
      }
    },
  },
};
</script>


<style>
@media only screen and (min-width: 950px) {
  .layout {
    display: grid;
    grid-template-columns: 5% 1fr;
    grid-gap: 20px;
  }
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