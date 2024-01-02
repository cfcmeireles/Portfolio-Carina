<template>
  <main class="flex justify-center items-center h-screen lg:relative">
    <div class="mx-5 lg:absolute">
      <h1
        class="text-lightblue text-2xl sm:text-3xl lg:text-4xl font-mono my-5 text-center"
      >
        Contact me
      </h1>
      <ContactForm />
    </div>
  </main>
</template>
    
<script>
export default {
  mounted() {
    document.body.classList.remove("gradient-body");
  },
};
</script>
    
<style scoped>
body {
  background-color: #202833;
}

main > div {
  top: 20%;
}
</style>