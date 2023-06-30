<template>
  <div>
    <HamburgerMenu />
    <NavBar />
    <transition name="fade">
      <NavBarWithName v-if="showNameBar" />
    </transition>
    <slot />
  </div>
</template>
  
  <script>
export default {
  data() {
    return {
      showNameBar: false,
    };
  },
  mounted() {
    document.body.classList.remove("gradient-body");
    this.showNameBar = true;
  },
};
</script>
  
  <style>
.fade-enter-active {
  transition: opacity 1.5s ease-in-out;
}

.fade-enter-from {
  opacity: 0;
}
</style>