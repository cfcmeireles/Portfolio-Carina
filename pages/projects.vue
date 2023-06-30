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
        <div class="project-one">
          <h2>Sign Up Form with Vue 3</h2>
          <iframe
            title="Sign Up Form with Vue 3"
            src="https://sign-up-form-cm.netlify.app/"
            height="100%"
            width="100%"
            frameborder="0"
          ></iframe>
          <p>
            In this project I had the opportunity to practice Vue 3 by building
            a Frontend Mentor challenge using forms
          </p>
        </div>
        <div class="project-two">
          <h2>To do app with Vue 3</h2>
          <iframe
            title="To do app with Vue 3"
            src="https://magenta-melba-71e7bd.netlify.app/"
            height="100%"
            width="100%"
            frameborder="0"
          ></iframe>
          <p>
            As my first Vue 3 project, I developed a simple to do app that
            allows users to add, remove and filter through priority list tasks
          </p>
        </div>
        <div class="project-three">
          <h2>Basketball Scoreboard with CSS grid and flex</h2>
          <iframe
            title="Basketball Scoreboard with CSS grid and flex"
            src="https://basketball-scoreboard-cm.netlify.app/"
            height="100%"
            width="100%"
            frameborder="0"
          ></iframe>
          <p>
            As part of a Scrimba course, I had the opportunity to develop extra
            features on a Basketball scoreboard app, allowing me to practice CSS
            grid and flex concepts in the process
          </p>
        </div>
        <div class="project-four">
          <h2>Game of Pig with JavaScript</h2>
          <iframe
            title="Game of Pig with JavaScript"
            src="https://game-of-pig1.netlify.app/"
            height="100%"
            width="100%"
            frameborder="0"
          ></iframe>
          <p>
            While learning JavaScript with Coursera, I had the chance to develop
            extra features on the classic Game of Pig, with extra players, score
            limit choice and more dice, I was able to improve my JavaScript
            skills
          </p>
        </div>
      </div>
    </div>
  </main>
</template>
    
<script>
definePageMeta({
  layout: "projects",
});
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
/* 
.project-preview {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
} */

img {
  height: 300px;
  width: 100%;
}

.project-one,
.project-two,
.project-three,
.project-four {
  height: 900px;
  width: 750px;
  margin-bottom: 150px;
}

h2,
.project-preview p {
  text-align: center;
}
</style>