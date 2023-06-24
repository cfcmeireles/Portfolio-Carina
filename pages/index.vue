<template>
  <main id="home-page">
    <div class="home">
      <transition name="fade">
        <h1 v-if="showName">Carina Meireles</h1>
      </transition>
      <div class="lol">
        <transition name="typewriter">
          <h2 v-if="showText">
            I am an aspiring developer based in Lisbon, Portugal
            <br />
          </h2>
        </transition>
        <transition name="typewriter">
          <h2 v-if="showText">Currently employed by Miniclip</h2>
        </transition>
      </div>
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
export default {
  data() {
    return {
      showName: false,
      showText: false,
      showIcons: false,
    };
  },
  mounted() {
    this.showName = true;
    setTimeout(() => {
      this.showText = true;
    }, 2000);
    setTimeout(() => {
      this.showIcons = true;
    }, 6000);
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
  height: 205px;
}

.lol {
  text-align: center;
}

.github-icon {
  width: 3%;
  padding-right: 10px;
}
.linkedin-icon {
  width: 3%;
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

.typewriter-enter-active {
  animation: typewriter 2s steps(40) 1s forwards;
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
}

.fadeIn-enter-active {
  transition: opacity 1.5s ease-in-out;
}
.fadeIn-enter-from {
  opacity: 0;
}
</style>