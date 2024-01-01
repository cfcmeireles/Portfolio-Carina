<template>
  <main class="h-full flex justify-center items-center">
    <div class="text-center mb-24">
      <h1
        class="mt-20 lg:mt-5 text-lightblue text-2xl sm:text-3xl lg:text-4xl font-mono my-5"
      >
        Projects
      </h1>
      <p class="mx-5 text-sm md:text-base my-4 font-rubik">
        In this section you will find some of the projects I've worked on, for
        more, you can also check my
        <NuxtLink
          class="text-lightblue"
          to="https://github.com/cfcmeireles"
          target="_blank"
          >GitHub page</NuxtLink
        >
      </p>
      <div
        class="project-frame flex flex-col items-center lg:grid lg:grid-cols-2 lg:flex-wrap lg:justify-center lg:items-start lg:gap-x-14 lg:gap-y-14"
      >
        <a
          href="https://github.com/cfcmeireles/advice-generator-app"
          target="_blank"
        >
          <Transition name="fade">
            <ProjectFrames
              :skills="{ html: true, css: true, nuxt: true }"
              :previews="{ projectOne: true }"
              v-if="showTransitionProjectOne"
            >
              <template #title>Advice Generator</template>
              <template #image>
                <img
                  src="../assets/projects/AdviceGenerator.png"
                  class="hidden md:block w-full h-full"
              /></template>
              <template #description>
                As a part of a Frontend Mentor Challenge, I used Advice Slip
                JSON API to build an app that provides users with life advice
              </template>
            </ProjectFrames>
          </Transition>
        </a>
        <a
          href="https://github.com/cfcmeireles/Password-generator"
          target="_blank"
        >
          <Transition name="fade">
            <ProjectFrames
              :skills="{ html: true, css: true, vue: true }"
              :previews="{ projectTwo: true }"
              v-if="showTransitionProjectTwo"
            >
              <template #title>Password Generator</template>
              <template #image
                ><img
                  src="../assets/projects/PasswordGenerator.png"
                  class="hidden md:block w-full h-full"
              /></template>
              <template #description>
                To keep on practicing Vue 3, I challenged myself to build a
                Password Generator app, a useful day to day tool
              </template>
            </ProjectFrames>
          </Transition>
        </a>
        <a href="https://github.com/cfcmeireles/to-do-app" target="_blank">
          <Transition name="fade">
            <ProjectFrames
              :skills="{ html: true, css: true, vue: true }"
              :previews="{ projectThree: true }"
              v-if="showTransitionProjectThree"
            >
              <template #title>To Do List</template>
              <template #image
                ><img
                  src="../assets/projects/ToDoList.png"
                  class="hidden md:block w-full h-full"
              /></template>
              <template #description>
                As my first Vue 3 project, I developed a simple to do list app
                that allows users to add, remove and filter through priority
                list tasks</template
              >
            </ProjectFrames>
          </Transition>
        </a>
        <a href="https://support.miniclip.com/hc/en-us" target="_blank">
          <Transition name="fade">
            <ProjectFrames
              :skills="{ html: true, css: true, js: true }"
              :previews="{ projectFour: true }"
              v-if="showTransitionProjectFour"
            >
              <template #title>Miniclip's Knowledge Base</template>
              <template #image
                ><img
                  src="../assets/projects/MiniclipKB.png"
                  class="hidden md:block w-full h-full"
              /></template>
              <template #description>
                As part of my training, I built Miniclip's player support
                website while learning HTML, CSS and JavaScript
              </template>
            </ProjectFrames>
          </Transition>
        </a>
      </div>
    </div>
  </main>
</template>

<script>
import ProjectFrames from "~/components/ProjectFrames.vue";
export default {
  ProjectFrames,
  data() {
    return {
      showTransitionProjectOne: false,
      showTransitionProjectTwo: false,
      showTransitionProjectThree: false,
      showTransitionProjectFour: false,
    };
  },
  mounted() {
    document.body.classList.remove("gradient-body");
    this.showTransitionProjectOne = true;
    setTimeout(() => {
      this.showTransitionProjectTwo = true;
    }, 1000);
    setTimeout(() => {
      this.showTransitionProjectThree = true;
    }, 2000);
    setTimeout(() => {
      this.showTransitionProjectFour = true;
    }, 3000);
  },
};
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 2s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

@media (max-width: 1400px) {
  .project-frame {
    display: flex;
    flex-direction: column;
    align-content: center;
  }
}
</style>
