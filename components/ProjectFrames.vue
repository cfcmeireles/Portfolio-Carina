<template>
  <div
    class="max-w-xl rounded-2xl max-h-full bg-gray-100 lg:hover:scale-105 lg:hover:duration-500 lg:hover:ease-in-out lg:hover:shadow-md"
  >
    <h2 class="text-xl lg:text-2xl font-bold my-3 py-5 font-rubik">
      <slot name="title"></slot>
    </h2>
    <slot name="image"></slot>
    <p class="text-sm md:text-base lg:text-lg mt-3 mx-5 font-rubik text-black">
      <slot name="description"></slot>
    </p>
    <div class="flex mx-auto mb-5 py-5 items-center justify-center">
      <img class="w-8 h-8" src="../assets/html-5.png" v-if="skills.html" />
      <img class="w-8 h-8" src="../assets/css-3.png" v-if="skills.css" />
      <img class="w-8 h-8" src="../assets/js.png" v-if="skills.js" />
      <img class="w-8 h-8" src="../assets/vue.png" v-if="skills.vue" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    skills: {
      type: Object,
      default: () => ({
        html: false,
        css: false,
        js: false,
        vue: false,
      }),
    },
  },
};
</script>
