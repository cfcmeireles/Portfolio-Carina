<template>
  <main id="projects-page">
    <div class="projects">
      <h1 class="section-titles">Projects</h1>
      <p>
        In this section you will find some of the projects I've worked on, for
        more, you can also check my
        <NuxtLink
          class="github-link"
          to="https://github.com/cfcmeireles"
          target="_blank"
          >GitHub page</NuxtLink
        >
      </p>
      <div class="project-preview">
        <Transition name="fade">
          <ProjectFrames v-if="showTransitionProjectOne">
            <template #title>Password Generator</template>
            <template #image
              ><img
                src="../assets/projects/PasswordGenerator.png"
                class="project-imgs"
            /></template>
            <template #description>
              In this project I had the opportunity to practice Vue 3 by
              building a useful Password Generator</template
            >
            <template #skills>
              <img class="skills-icons" src="../assets/html-5.png" />
              <img class="skills-icons" src="../assets/css-3.png" />
              <img class="skills-icons" src="../assets/vue.png" />
            </template>
          </ProjectFrames>
        </Transition>
        <Transition name="fade">
          <ProjectFrames v-if="showTransitionProjectTwo">
            <template #title>To do app</template>
            <template #image
              ><img src="../assets/projects/ToDoList.png" class="project-imgs"
            /></template>
            <template #description>
              As my first Vue 3 project, I developed a simple to do app that
              allows users to add, remove and filter through priority list
              tasks</template
            >
            <template #skills>
              <img class="skills-icons" src="../assets/html-5.png" />
              <img class="skills-icons" src="../assets/css-3.png" />
              <img class="skills-icons" src="../assets/vue.png" />
            </template>
          </ProjectFrames>
        </Transition>
        <Transition name="fade">
          <ProjectFrames v-if="showTransitionProjectThree">
            <template #title>Miniclip's Knowledge Base</template>
            <template #image
              ><img
                src="../assets/projects/MiniclipKB.png"
                class="project-imgs"
            /></template>
            <template #description>
              As part of my training, I had the chance to practice solid basics
              of HTML, CSS and JavaScript while completely revamping the support
              website for Miniclip</template
            >
            <template #skills>
              <img class="skills-icons" src="../assets/html-5.png" />
              <img class="skills-icons" src="../assets/css-3.png" />
              <img class="skills-icons" src="../assets/js.png" />
            </template>
          </ProjectFrames>
        </Transition>
        <Transition name="fade">
          <ProjectFrames v-if="showTransitionProjectFour">
            <template #title>Basketball Scoreboard</template>
            <template #image
              ><img
                src="../assets/projects/BasketballScoreboard.png"
                class="project-imgs"
            /></template>
            <template #description>
              As part of a Scrimba course, I developed extra features on a
              Basketball scoreboard app, allowing me to practice CSS grid and
              flex concepts in the process</template
            >
            <template #skills>
              <img class="skills-icons" src="../assets/html-5.png" />
              <img class="skills-icons" src="../assets/css-3.png" />
              <img class="skills-icons" src="../assets/js.png" />
            </template>
          </ProjectFrames>
        </Transition>
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
#projects-page {
  display: flex;
  align-content: center;
  justify-content: center;
}
.github-link {
  text-decoration: none;
}

.projects {
  text-align: center;
  margin-bottom: 100px;
}
.project-preview {
  display: flex;
  flex-direction: column;
  align-items: center;
}

@media only screen and (min-width: 1650px) {
  .project-preview {
    display: grid;
    grid-template-columns: 1fr 1fr;
    /* flex-direction: column; */
    /* columns: 2; */
    flex-wrap: wrap;
    /* grid-template-columns: repeat(auto-fit, minmax(600px, 1fr)); */
    justify-content: center;
    align-items: flex-start;
    column-gap: 5%;
    row-gap: 5%;
  }
}

/* img {
  height: 300px;
  width: 100%;
} */

.project-imgs {
  width: 100%;
  height: 100%;
}

.skills-bar {
  display: flex;
  border: 1px solid lightgray;
  border-radius: 15px;
  background: grey;
  width: 50%;
  margin: 0 auto;
  margin-bottom: 20px;
  padding: 5px;
  justify-content: center;
  align-items: center;
}

.skills-icons {
  width: 10%;
  height: 10%;
}

h2,
.project-preview p {
  text-align: center;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 2s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>