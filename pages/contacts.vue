<template>
  <body class="bg-darkblue font-rubik">
    <main class="flex items-center justify-center h-screen">
      <div>
        <h1 class="text-lightblue text-4xl font-mono my-5">Contact me</h1>
        <form>
          <FormInput
            id="name"
            label="Name"
            placeholder="Your name"
            type="text"
          />
          <FormInput
            id="email"
            label="Email"
            placeholder="Your email"
            type="email"
          />
          <FormInput
            id="subject"
            label="Subject"
            placeholder="Write here"
            type="textarea"
          />
          <FormInput type="submit" />
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
    