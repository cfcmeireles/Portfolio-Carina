<template>
  <body class="bg-darkblue font-rubik">
    <main class="flex items-center justify-center h-screen">
      <div class="mx-5">
        <h1 class="text-lightblue text-4xl font-mono my-5">Contact me</h1>
        <form>
          <ContactForm />
        </form>
      </div>
    </main>
  </body>
</template>
    
<script>
export default {
  mounted() {
    document.body.classList.remove("gradient-body");
  },
};
</script>
    