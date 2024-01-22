<template>
  <div
    class="mx-10 md:mx-0 max-w-xl rounded-2xl bg-gray-100"
    :class="isPageLoaded ? 'hover-effect' : ''"
    @readyForHover="readyForHover"
  >
    <h2 class="text-xl lg:text-2xl font-bold my-3 py-5 font-rubik">
      <slot name="title"></slot>
    </h2>
    <slot name="image"></slot>
    <p
      class="text-sm md:text-base mt-3 mx-5 font-rubik text-black h-32 sm:h-20 flex items-center justify-center"
    >
      <slot name="description"></slot>
    </p>

    <div class="flex mx-auto mb-5 py-5 items-center justify-center relative">
      <img
        class="w-8 h-8"
        src="../assets/html-5.png"
        alt="HTML Icon"
        v-if="skills.html"
      />
      <img
        class="w-8 h-8"
        src="../assets/css-3.png"
        alt="CSS Icon"
        v-if="skills.css"
      />
      <img
        class="w-8 h-8"
        src="../assets/js.png"
        alt="JavaScript Icon"
        v-if="skills.js"
      />
      <img
        class="w-8 h-8"
        src="../assets/vue.png"
        alt="Vue Icon"
        v-if="skills.vue"
      />
      <img
        class="w-8 h-8"
        src="../assets/nuxt.png"
        alt="Nuxt Icon"
        v-if="skills.nuxt"
      />
      <a
        href="https://advice-generator-app-cm.netlify.app/"
        target="_blank"
        v-if="previews.projectOne"
      >
        <img
          src="../assets/expand-icon.svg"
          class="h-5 absolute right-3 bottom-3"
          alt="Linkedin Logo"
        />
      </a>
      <a
        href="https://password-generator-app-cm.netlify.app/"
        target="_blank"
        v-if="previews.projectTwo"
      >
        <img
          src="../assets/expand-icon.svg"
          class="h-5 absolute right-3 bottom-3"
          alt="Linkedin Logo"
        />
      </a>
      <a
        href="https://to-do-app-cm.netlify.app/"
        target="_blank"
        v-if="previews.projectThree"
      >
        <img
          src="../assets/expand-icon.svg"
          class="h-5 absolute right-3 bottom-3"
          alt="Linkedin Logo"
        />
      </a>
      <a
        href="https://support.miniclip.com/hc/en-us"
        target="_blank"
        v-if="previews.projectFour"
      >
        <img
          src="../assets/expand-icon.svg"
          class="h-5 absolute right-3 bottom-3"
          alt="Linkedin Logo"
        />
      </a>
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
    previews: {
      type: Object,
      default: () => ({
        projectOne: false,
        projectTwo: false,
        projectThree: false,
        projectFour: false,
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