<template>
  <main class="flex items-center justify-center h-screen">
    <div class="contacts">
      <h1 class="text-lightblue text-4xl font-mono my-5">Contact me</h1>
      <form>
        <label for="name">Name</label>
        <input
          class="w-full p-3 border-2 border-gray-400 rounded box-border mt-1.5 mb-4 resize-y"
          type="text"
          id="name"
          placeholder="Your name"
        />
        <label for="email">Email</label>
        <input
          class="w-full p-3 border-2 border-gray-400 rounded box-border mt-1.5 mb-4 resize-y"
          type="text"
          id="email"
          placeholder="Your email"
        />
        <label for="subject">Subject</label>
        <textarea
          class="w-full p-3 border-2 border-gray-400 rounded box-border mt-1.5 mb-4 resize-y"
          id="subject"
          placeholder="Write here"
        ></textarea>
        <input
          class="py-3 px-5 rounded cursor-pointer text-white bg-green-300 hover:bg-green-500"
          type="submit"
          value="Submit"
          @click.prevent="mailto"
        />
      </form>
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
    
    <style>
body {
  font-family: "Rubik", sans-serif;
}
</style>