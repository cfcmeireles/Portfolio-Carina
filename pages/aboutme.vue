<template>
  <main id="about-me-page">
    <div class="about-me">
      <h1 class="section-titles">About me</h1>
      <div class="about-me-text">
        <div>
          <h2>Hi, I'm <strong>Carina</strong></h2>
          <p>
            I'm an aspiring Web Developer with 1 year of learning experience.
            I'm from Lisbon and I love technology and gaming.
          </p>
          <p>
            My goal is to develop interactive, responsive software that
            seamlessly engages users and adapts to their needs, while providing
            invaluable functionality. Lorem ipsum dolor sit amet, consectetur
            adipisicing elit. Tempore, nostrum. Repellat, ratione. Rem placeat
            quis sequi possimus ea magni corporis?
          </p>
        </div>
        <div>
          <h2>What is my skill level?</h2>
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Est
            repudiandae voluptas tenetur veritatis officiis reprehenderit
            architecto iure corrupti error dolore. Lorem ipsum dolor sit, amet
            consectetur adipisicing elit. Est repudiandae voluptas tenetur
            veritatis officiis reprehenderit architecto iure corrupti error
            dolore.
          </p>
          <p>
            At the moment, I am still building a solid foundation in Front-end
            development.
          </p>
        </div>
      </div>
      <h3>My current tech stack:</h3>
      <div class="gallery">
        <img class="image" src="../assets/html-5.png" height="80" />

        <img src="../assets/css-3.png" height="80" />

        <img src="../assets/tailwind.png" height="80" />

        <img src="../assets/js.png" height="80" />

        <img src="../assets/vue.png" height="80" />

        <img src="../assets/nuxt-3.png" height="80" />
      </div>
    </div>
  </main>
</template>
  
<script>
</script>
  
<style>
@import "../app.css";

@media only screen and (min-width: 1451px) {
  .about-me-text {
    display: grid;
    grid-template-columns: 600px 600px;
  }

  .gallery {
    margin-top: 50px;
    display: grid;
    grid-template-columns: repeat(3, 300px);
    row-gap: 70px;
    justify-content: center;
  }

  .gallery img {
    display: flex;
    margin: 0 auto;
  }

  p {
    line-height: 1.5;
  }
}

@media only screen and (max-width: 1450px) {
  .about-me {
    width: 50%;
  }

  .about-me-text {
    display: grid;
    grid-template-rows: repeat(2, 1fr);
  }

  .gallery {
    margin-top: 50px;
    display: grid;
    grid-template-columns: repeat(3, 200px);
    row-gap: 20px;
    justify-content: center;
  }

  .gallery img {
    display: flex;
    height: 60px;
    margin: 0 auto;
  }

  p {
    line-height: 1.5;
  }
}

@media only screen and (max-width: 950px) {
  h1 {
    margin-top: 100px;
  }

  .about-me {
    width: 100%;
    height: 100%;
  }

  .about-me-text {
    display: grid;
    grid-template-rows: repeat(2, 1fr);
  }

  .gallery {
    margin-top: 50px;
    display: grid;
    grid-template-columns: repeat(3, 100px);
    row-gap: 20px;
    justify-content: center;
  }

  .gallery img {
    display: flex;
    height: 60px;
    margin: 0 auto;
  }

  p {
    line-height: 1.5;
  }
}

/* .container {
  width: 80%;
  background-color: #ddd;
  margin-bottom: 10px;
} */

/* .skills {
  padding-top: 10px;
  padding-bottom: 10px;
  background-color: blue;
} */

/* .html {
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
    width: 50%;
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
} */
</style>