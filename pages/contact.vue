<template>
  <body class="bg-darkblue font-rubik">
    <main class="flex items-center justify-center h-screen">
      <div class="mx-5">
        <h1
          class="text-lightblue text-2xl sm:text-3xl lg:text-4xl font-mono my-5 text-center mb-20 -mt-20 sm:mt-0"
        >
          Contact me
        </h1>
        <ContactForm />
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
    