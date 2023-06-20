<template>
  <div>
    <HamburgerMenu />
    <NavBarWithName />
    <slot />
  </div>
</template>

<script>
export default {
  mounted() {
    document.body.classList.remove("gradient-body");
  },
};
</script>
