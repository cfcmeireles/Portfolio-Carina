<template>
  <main class="h-screen flex items-center justify-center">
    <div class="text-center" style="height: 500px">
      <transition name="fade">
        <img class="w-52" v-if="showPhoto" src="../assets/kina_avatar.png" />
      </transition>

      <transition name="fade">
        <h1 class="font-mulish text-lightblue text-4xl my-2.5" v-if="showName">
          CARINA MEIRELES
        </h1>
      </transition>
      <VueWriter
        v-if="showText"
        :array="['I am an aspiring developer based in Lisbon, Portugal']"
        :iterations="1"
        :typeSpeed="50"
        class="text-sm leading-8 text-white font-mono"
      />
      <VueWriter
        v-if="showText2"
        :array="['Currently employed by Miniclip']"
        :iterations="1"
        :typeSpeed="50"
        class="text-sm leading-8 text-white font-mono"
      />
      <transition name="fadeIn">
        <div v-if="showIcons">
          <NuxtLink to="https://github.com/cfcmeireles" target="_blank">
            <img
              src="../assets/github-icon.svg"
              class="pr-2.5 mt-2.5"
              alt="GitHub Logo"
            />
          </NuxtLink>
          <NuxtLink
            to="https://www.linkedin.com/in/carina-meireles/"
            target="_blank"
          >
            <img src="../assets/linkedin-icon.svg" alt="Linkedin Logo" />
          </NuxtLink>
        </div>
      </transition>
    </div>
  </main>
</template>

<script>
import VueWriter from "vue-writer";
export default {
  components: { VueWriter },
  data() {
    return {
      showPhoto: false,
      showName: false,
      showText: false,
      showText2: false,
      showIcons: false,
    };
  },
  mounted() {
    document.body.classList.add("gradient-body");
    this.showPhoto = true;
    this.showName = true;
    setTimeout(() => {
      this.showText = true;
    }, 2000);
    setTimeout(() => {
      this.showText2 = true;
    }, 5000);
    setTimeout(() => {
      this.showIcons = true;
    }, 7000);
  },
};
</script>

<style>
@import "../tailwind.css";

.gradient-body {
  background: linear-gradient(-45deg, #46a29f, #202833);
  background-size: 400% 400%;
  animation: gradient 15s ease infinite;
  height: 100vh;
}

.fade-enter-active {
  animation: fadeIn 2s;
}

.fade-leave-active {
  animation: fadeIn 0.5s reverse;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
  transform: translateY(-20px);
}

@keyframes fadeIn {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}
.fadeIn-enter-active {
  transition: opacity 1.5s ease-in-out;
}
.fadeIn-enter-from {
  opacity: 0;
}
</style>