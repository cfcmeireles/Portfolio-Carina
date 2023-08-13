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
            <a
              href="http://courageous-paletas-8356a0.netlify.app/"
              target="_blank"
            >
              <h2>Password Generator</h2>
              <img
                src="../assets/projects/PasswordGenerator.png"
                class="project-imgs"
              />
              <p>
                In this project I had the opportunity to practice Vue 3 by
                building a useful Password Generator
              </p>
              <div class="skills-bar">
                <p>Skills used:</p>
                <img class="skills-icons" src="../assets/html-5.png" />
                <img class="skills-icons" src="../assets/css-3.png" />
                <img class="skills-icons" src="../assets/vue.png" />
              </div>
            </a>
          </div>
        </Transition>
        <Transition name="fade">
          <div class="project-two" v-if="showTransitionProjectTwo">
            <a href="http://magenta-melba-71e7bd.netlify.app" target="_blank">
              <h2>To do app</h2>
              <img src="../assets/projects/ToDoList.png" class="project-imgs" />
              <p>
                As my first Vue 3 project, I developed a simple to do app that
                allows users to add, remove and filter through priority list
                tasks
              </p>
              <div class="skills-bar">
                <p>Skills used:</p>
                <img class="skills-icons" src="../assets/html-5.png" />
                <img class="skills-icons" src="../assets/css-3.png" />
                <img class="skills-icons" src="../assets/vue.png" />
              </div>
            </a>
          </div>
        </Transition>
        <Transition name="fade">
          <div class="project-three" v-if="showTransitionProjectThree">
            <a href="https://support.miniclip.com/hc/en-us" target="_blank">
              <h2>Miniclip's Knowledge Base</h2>
              <img
                class="project-imgs"
                src="../assets/projects/MiniclipKB.png"
              />
              <p>
                As part of my training, I had the chance to practice solid
                basics of HTML, CSS and JavaScript while completely revamping
                the support website for Miniclip
              </p>
              <div class="skills-bar">
                <p>Skills used:</p>
                <img class="skills-icons" src="../assets/html-5.png" />
                <img class="skills-icons" src="../assets/css-3.png" />
                <img class="skills-icons" src="../assets/js.png" />
              </div>
            </a>
          </div>
        </Transition>
        <Transition name="fade">
          <div class="project-four" v-if="showTransitionProjectFour">
            <a
              href="http://basketball-scoreboard-cm.netlify.app"
              target="_blank"
            >
              <h2>Basketball Scoreboard</h2>
              <img
                src="../assets/projects/BasketballScoreboard.png"
                class="project-imgs"
              />
              <p>
                As part of a Scrimba course, I developed extra features on a
                Basketball scoreboard app, allowing me to practice CSS grid and
                flex concepts in the process
              </p>
              <div class="skills-bar">
                <p>Skills used:</p>
                <img class="skills-icons" src="../assets/html-5.png" />
                <img class="skills-icons" src="../assets/css-3.png" />
                <img class="skills-icons" src="../assets/js.png" />
              </div>
            </a>
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
.project-preview {
  display: flex;
  flex-direction: column;
  align-items: center;
}

@media only screen and (max-width: 1650px) {
  .project-one,
  .project-two,
  .project-three,
  .project-four {
    margin-bottom: 20px;
  }
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

  .project-one:hover,
  .project-two:hover,
  .project-three:hover,
  .project-four:hover {
    transform: scale(1.1);
    transition: ease-in-out 0.5s;
    box-shadow: 0 3px 3px rgba(0, 0, 0, 0.2);
  }
}

.projects {
  margin-bottom: 100px;
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
  border: 1px solid black;
  border-radius: 15px;
  background-color: lightgrey;
  max-height: 100%;
  cursor: pointer;
  transition: transform 0.3s, margin 0.3s;
}
/* .project-one:hover,
.project-two:hover {
  margin-top: 40px;
} */

.project-one p,
.project-two p,
.project-three p,
.project-four p {
  color: black;
}
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

a {
  text-decoration: none;
  color: black;
}
</style>