<template>
  <div
    class="max-w-xl rounded-2xl max-h-full bg-gray-100"
    :class="isPageLoaded ? 'hover-effect' : ''"
    @readyForHover="readyForHover"
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
      <img class="w-8 h-8" src="../assets/nuxt.png" v-if="skills.nuxt" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isPageLoaded: false,
    };
  },
  mounted() {
    this.readyForHover();
  },
  props: {
    skills: {
      type: Object,
      default: () => ({
        html: false,
        css: false,
        js: false,
        vue: false,
        nuxt: false,
      }),
    },
  },
  methods: {
    readyForHover() {
      setTimeout(() => {
        this.isPageLoaded = true;
      }, 3000);
    },
  },
};
</script>

<style>
@media (min-width: 1024px) {
  .hover-effect:hover {
    --tw-scale-x: 1.05;
    --tw-scale-y: 1.05;
    transform: translate(var(--tw-translate-x), var(--tw-translate-y))
      rotate(var(--tw-rotate)) skewX(var(--tw-skew-x)) skewY(var(--tw-skew-y))
      scaleX(var(--tw-scale-x)) scaleY(var(--tw-scale-y));
    transition-duration: 500ms;
    transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
    --tw-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1),
      0 2px 4px -2px rgb(0 0 0 / 0.1);
    --tw-shadow-colored: 0 4px 6px -1px var(--tw-shadow-color),
      0 2px 4px -2px var(--tw-shadow-color);
    box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000),
      var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow);
  }
}
</style>