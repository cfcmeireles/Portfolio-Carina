<template>
  <main class="flex justify-center h-screen lg:relative">
    <div class="mx-5 lg:absolute">
      <h1
        class="text-lightblue text-2xl sm:text-3xl lg:text-4xl font-mono my-5 text-center mt-20 lg:mt-0"
      >
        About me
      </h1>
      <div
        class="about-me flex flex-col justify-center sm:max-w-screen-sm md:max-w-screen-md lg:max-w-full lg:w-full lg:grid lg:gap-36"
        style="grid-template-columns: 600px 600px"
      >
        <div>
          <h2
            class="pb-5 md:pb-0 text-xl lg:text-2xl my-5 text-white font-rubik"
          >
            Hi, I'm <strong>Carina</strong>
          </h2>
          <p
            class="text-sm md:text-base sm:!leading-loose md:!leading-loose lg:!leading-loose font-rubik"
          >
            I'm a budding Web Developer, currently employed by Miniclip. For the
            past year, I've been immersed in the exciting world of web
            development, driven by my fascination with how technology can
            simplify our lives.
          </p>
          <p
            class="text-sm md:text-base leading-normal font-rubik sm:!leading-loose md:!leading-loose lg:!leading-loose"
          >
            My mission? To use technology creatively and practically to solve
            real-life challenges for businesses since I believe in the power of
            web development to make a positive impact.
          </p>
        </div>
        <div>
          <h2
            class="pb-5 md:pb-0 text-xl lg:text-2xl my-5 text-white font-rubik"
          >
            What can I do?
          </h2>
          <p
            class="text-sm md:text-base leading-normal font-rubik sm:!leading-loose md:!leading-loose lg:!leading-loose"
          >
            Over the past year, I've been honing my skills by working on various
            projects. From making the player support website for Miniclip using
            vanilla Javascript to tackling personal projects with frameworks
            such as Vue 3 and Nuxt 3, I've been deeply engaged in the front-end
            technologies that bring digital experiences to life.
          </p>
        </div>
      </div>
      <h3 class="tech-stack text-xl lg:text-2xl my-5 text-white font-rubik">
        My current tech stack:
      </h3>
      <div
        class="fade-in-element flex flex-wrap pt-10 pb-10 md:w-full lg:pt-0 lg:mt-12 lg:grid lg:text-center lg:justify-center lg:w-full icons"
        style="row-gap: 70px; grid-template-columns: 300px 300px 300px"
      >
        <img
          class="h-10 lg:h-16 flex mx-auto"
          src="../assets/html-5.png"
          alt="HTML Icon"
        />

        <img
          class="h-10 lg:h-16 flex mx-auto"
          src="../assets/css-3.png"
          alt="CSS Icon"
        />

        <img
          class="h-10 lg:h-16 flex mx-auto"
          src="../assets/tailwind.png"
          alt="Tailwind Icon"
        />

        <img
          class="h-10 lg:h-16 flex mx-auto"
          src="../assets/js.png"
          alt="JavaScript Icon"
        />

        <img
          class="h-10 lg:h-16 flex mx-auto"
          src="../assets/vue.png"
          alt="Vue Icon"
        />

        <img
          class="h-10 lg:h-16 flex mx-auto"
          src="../assets/nuxt.png"
          alt="Nuxt Icon"
        />
      </div>
    </div>
  </main>
</template>

<script>
export default {
  mounted() {
    document.body.classList.remove("gradient-body");
  },
};
</script>

<style scoped>
@import "../tailwind.css";

body {
  background-color: #202833;
}

@keyframes fade-in {
  0% {
    opacity: 0;
    transform: translate(-1%, -1%);
  }
  100% {
    opacity: 1;
    transform: translateY(0, 0);
  }
}

.fade-in-element {
  animation: fade-in 2s ease-out;
}

@media (max-width: 1024px) {
  .fade-in-element {
    animation: fade-in 5s ease-out;
  }
}

@media (min-width: 1024px) and (max-width: 1390px) {
  .about-me {
    display: flex;
    flex-direction: column;
    gap: 0;
  }
}

@media (min-width: 1391px) and (max-width: 1500px) {
  .about-me {
    column-gap: 1rem;
  }
}

@media (min-width: 1391px) and (max-width: 1440px) {
  .about-me {
    margin-left: 25px;
  }

  .tech-stack {
    margin-left: 35px;
  }
}

@media (min-width: 1501px) and (max-width: 1550px) {
  .about-me {
    margin-left: 25px;
  }

  .tech-stack {
    margin-left: 35px;
  }
}

@media (min-width: 768px) and (max-width: 1390px) {
  main > div {
    margin: 5rem !important;
    top: 0 !important;
  }
}

main > div {
  top: 20%;
}
</style>
