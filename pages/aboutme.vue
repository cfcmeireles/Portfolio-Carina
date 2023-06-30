<template>
  <main id="about-me-page">
    <div class="about-me">
      <h1 class="section-titles">About me</h1>
      <div class="about-me-text">
        <div>
          <h2>Hi, I'm <strong>Carina Meireles</strong></h2>
          <p>
            I'm an aspiring Web Developer with 1 year of learning experience.
            I'm from Lisbon and I love technology and gaming.
          </p>
          <p>
            My goal is to develop interactive, responsive software that
            seamlessly engages users and adapts to their needs, while providing
            invaluable functionality.
          </p>
        </div>
        <div>
          <h2>What is my skill level?</h2>
          <p>
            At the moment, I am still building a solid foundation in Front-end
            development, my current skills are:
          </p>
        </div>
      </div>
      <img src="../assets/html-5.png" height="50" />
      <div class="container">
        <div class="skills html"></div>
      </div>
      <img src="../assets/css-3.png" height="50" />
      <div class="container">
        <div class="skills css"></div>
      </div>
      <img src="../assets/js.png" height="50" />
      <div class="container">
        <div class="skills js"></div>
      </div>
      <img src="../assets/vue.png" height="50" />
      <div class="container">
        <div class="skills vue"></div>
      </div>
      <img src="../assets/nuxt.png" height="30" />
      <div class="container">
        <div class="skills nuxt"></div>
      </div>
    </div>
  </main>
</template>
  
<script>
definePageMeta({
  layout: "aboutme",
});
</script>
  
<style>
@import "../app.css";

.about-me-text {
  display: grid;
  grid-template-columns: 600px 600px;
}

.container {
  width: 80%;
  background-color: #ddd;
  margin-bottom: 10px;
}

.skills {
  padding-top: 10px;
  padding-bottom: 10px;
  background-color: blue;
}

.html {
  width: 0;
  animation: html-fill 2s forwards;
}

@keyframes html-fill {
  100% {
    width: 90%;
  }
}

.css {
  width: 0;
  animation: css-fill 2s forwards;
}

@keyframes css-fill {
  100% {
    width: 80%;
  }
}

.js {
  width: 0;
  animation: js-fill 2s forwards;
}

@keyframes js-fill {
  100% {
    width: 70%;
  }
}

.vue {
  width: 0;
  animation: vue-fill 2s forwards;
}

@keyframes vue-fill {
  100% {
    width: 30%;
  }
}

.nuxt {
  width: 0;
  animation: nuxt-fill 2s forwards;
}

@keyframes nuxt-fill {
  100% {
    width: 30%;
  }
}
</style>