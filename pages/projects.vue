<template>
  <body class="bg-darkblue">
    <main class="h-full flex items-center justify-center">
      <div class="text-center mb-24">
        <h1 class="text-lightblue text-4xl font-mono my-5">Projects</h1>
        <p class="my-4 font-rubik">
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
          class="flex flex-col items-center lg:grid lg:grid-cols-2 lg:flex-wrap lg:justify-center lg:items-start lg:gap-x-14 lg:gap-y-14"
        >
          <a
            href="https://github.com/cfcmeireles/Password-generator"
            target="_blank"
          >
            <Transition name="fade">
              <ProjectFrames v-if="showTransitionProjectOne">
                <template #title>Password Generator</template>
                <template #image
                  ><img
                    src="../assets/projects/PasswordGenerator.png"
                    class="w-full h-full"
                /></template>
                <template #description>
                  In this project I had the opportunity to practice Vue 3 by
                  building a useful Password Generator</template
                >
                <template #skills>
                  <img class="w-8 h-8" src="../assets/html-5.png" />
                  <img class="w-8 h-8" src="../assets/css-3.png" />
                  <img class="w-8 h-8" src="../assets/vue.png" />
                </template>
              </ProjectFrames>
            </Transition>
          </a>
          <a href="https://github.com/cfcmeireles/to-do-app" target="_blank">
            <Transition name="fade">
              <ProjectFrames v-if="showTransitionProjectTwo">
                <template #title>To do app</template>
                <template #image
                  ><img
                    src="../assets/projects/ToDoList.png"
                    class="w-full h-full"
                /></template>
                <template #description>
                  As my first Vue 3 project, I developed a simple to do app that
                  allows users to add, remove and filter through priority list
                  tasks</template
                >
                <template #skills>
                  <img class="w-8 h-8" src="../assets/html-5.png" />
                  <img class="w-8 h-8" src="../assets/css-3.png" />
                  <img class="w-8 h-8" src="../assets/vue.png" />
                </template>
              </ProjectFrames>
            </Transition>
          </a>
          <a href="https://support.miniclip.com/hc/en-us" target="_blank">
            <Transition name="fade">
              <ProjectFrames v-if="showTransitionProjectThree">
                <template #title>Miniclip's Knowledge Base</template>
                <template #image
                  ><img
                    src="../assets/projects/MiniclipKB.png"
                    class="w-full h-full"
                /></template>
                <template #description>
                  As part of my training, I had the chance to practice solid
                  basics of HTML, CSS and JavaScript while completely revamping
                  the support website for Miniclip</template
                >
                <template #skills>
                  <img class="w-8 h-8" src="../assets/html-5.png" />
                  <img class="w-8 h-8" src="../assets/css-3.png" />
                  <img class="w-8 h-8" src="../assets/js.png" />
                </template>
              </ProjectFrames>
            </Transition>
          </a>
          <a
            href="https://github.com/cfcmeireles/Basketball-Scoreboard"
            target="_blank"
          >
            <Transition name="fade">
              <ProjectFrames v-if="showTransitionProjectFour">
                <template #title>Basketball Scoreboard</template>
                <template #image
                  ><img
                    src="../assets/projects/BasketballScoreboard.png"
                    class="w-full h-full"
                /></template>
                <template #description>
                  As part of a Scrimba course, I developed extra features on a
                  Basketball scoreboard app, allowing me to practice CSS grid
                  and flex concepts in the process</template
                >
                <template #skills>
                  <img class="w-8 h-8" src="../assets/html-5.png" />
                  <img class="w-8 h-8" src="../assets/css-3.png" />
                  <img class="w-8 h-8" src="../assets/js.png" />
                </template>
              </ProjectFrames>
            </Transition>
          </a>
        </div>
      </div>
    </main>
  </body>
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
    
<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 2s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>