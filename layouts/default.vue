<template>
  <div class="layout">
    <div class="nav-bars">
      <HamburgerMenu
        @updateIsPageLoaded="updateIsPageLoaded"
        :isPageLoaded="isPageLoaded"
      />
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
    this.updateIsPageLoaded();
    this.handleClassChanged();
  },
  data() {
    return {
      timeOut: null,
      showNameBar: true,
      isPageLoaded: false,
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
    updateIsPageLoaded() {
      if (this.$route.path === "/" || this.$route.path === "/projects") {
        setTimeout(() => {
          this.isPageLoaded = true;
        }, 2000);
        this.isPageLoaded = false;
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