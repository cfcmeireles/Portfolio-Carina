<template>
  <main id="home-page">
    <div class="home">
      <transition name="fade">
        <img class="photo" v-if="showPhoto" src="../assets/kina_avatar.png" />
      </transition>

      <transition name="fade">
        <h1 class="fullname" v-if="showName">CARINA MEIRELES</h1>
      </transition>
      <VueWriter
        v-if="showText"
        :array="['I am an aspiring developer based in Lisbon, Portugal']"
        :iterations="1"
        :typeSpeed="50"
        class="writer-text"
      />
      <VueWriter
        v-if="showText2"
        :array="['Currently employed by Miniclip']"
        :iterations="1"
        :typeSpeed="50"
        class="writer-text"
      />
      <transition name="fadeIn">
        <div v-if="showIcons">
          <NuxtLink to="https://github.com/cfcmeireles" target="_blank">
            <img
              src="../assets/github-logo.png"
              class="github-icon"
              alt="GitHub Logo"
            />
          </NuxtLink>
          <NuxtLink
            to="https://www.linkedin.com/in/carina-meireles/"
            target="_blank"
          >
            <img
              src="../assets/linkedin-logo.png"
              class="linkedin-icon"
              alt="Linkedin Logo"
            />
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
      arr: "hello",
      showPhoto: false,
      showName: false,
      showText: false,
      showText2: false,
      showIcons: false,
    };
  },
  mounted() {
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

<style scoped>
#home-page {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.home {
  text-align: center;
  /* height: 490px; */
  height: 50vh;
}

h1 {
  margin-top: 10px;
  margin-bottom: 10px;
}
.photo {
  width: 200px;
  /* border: 5px solid #66fcf1; */
}

.writer-text {
  font-size: 0.9em;
  line-height: 2em;
  color: white;
  font-family: "Space Mono", monospace;
}

.github-icon {
  /* width: 2.5%; */
  height: 40px;
  padding-right: 10px;
  margin-top: 10px;
}
.linkedin-icon {
  height: 40px;
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
/* 
.typewriter-enter-active {
  animation: typewriter 2s steps(40);
  overflow: hidden;
  white-space: nowrap;
}

@keyframes typewriter {
  from {
    width: 0;
  }
  to {
    width: 100%;
  }
} */

.fadeIn-enter-active {
  transition: opacity 1.5s ease-in-out;
}
.fadeIn-enter-from {
  opacity: 0;
}
</style>