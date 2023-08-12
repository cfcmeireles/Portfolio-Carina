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
          <div class="project-one" v-if="showTransitionProjectOne">
            <h2>Password Generator with Vue 3</h2>
            <a
              href="http://courageous-paletas-8356a0.netlify.app/"
              target="_blank"
            >
              <img
                src="../assets/projects/PasswordGenerator.png"
                class="project-imgs"
              />
            </a>
            <p>
              In this project I had the opportunity to practice Vue 3 by
              building a Password Generator
            </p>
          </div>
        </Transition>
        <Transition name="fade">
          <div class="project-two" v-if="showTransitionProjectTwo">
            <h2>To do app with Vue 3</h2>
            <a href="http://magenta-melba-71e7bd.netlify.app" target="_blank">
              <img src="../assets/projects/ToDoList.png" class="project-imgs" />
            </a>
            <p>
              As my first Vue 3 project, I developed a simple to do app that
              allows users to add, remove and filter through priority list tasks
            </p>
          </div>
        </Transition>
        <Transition name="fade">
          <div class="project-three" v-if="showTransitionProjectThree">
            <h2>Basketball Scoreboard with CSS grid and flex</h2>
            <a
              href="http://basketball-scoreboard-cm.netlify.app"
              target="_blank"
            >
              <img
                src="../assets/projects/BasketballScoreboard.png"
                class="project-imgs"
              />
            </a>
            <p>
              As part of a Scrimba course, I had the opportunity to develop
              extra features on a Basketball scoreboard app, allowing me to
              practice CSS grid and flex concepts in the process
            </p>
          </div>
        </Transition>
        <Transition name="fade">
          <div class="project-four" v-if="showTransitionProjectFour">
            <h2>Game of Pig with JavaScript</h2>
            <a href="http://game-of-pig-v2.netlify.app/" target="_blank">
              <img
                src="../assets/projects/GameOfPig.png"
                class="project-imgs"
              />
            </a>
            <p>
              While learning JavaScript with Coursera, I had the chance to
              develop extra features on the classic Game of Pig, with extra
              players, score limit choice and more dice, I was able to improve
              my JavaScript skills
            </p>
          </div>
        </Transition>
      </div>
    </div>
  </main>
</template>
    
<script>
export default {
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
  }
}

/* img {
  height: 300px;
  width: 100%;
} */

.project-one,
.project-two,
.project-three,
.project-four {
  /* height: 900px;
  width: 750px; */
  /* margin-bottom: 150px; */
  /* display: flex; */
  /* max-width: 100%; */
  max-width: 600px;
}
.project-imgs {
  width: 100%;
  height: 100%;
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