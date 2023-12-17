<template>
  <body class="bg-darkblue">
    <main class="h-screen flex items-center justify-center">
      <div class="m-20">
        <h1 class="text-lightblue text-4xl font-mono my-5">About me</h1>
        <div
          class="flex flex-col w-screen sm:max-w-screen-sm md:max-w-screen-md lg:max-w-full lg:w-full lg:grid"
          style="grid-template-columns: repeat(auto-fill, minmax(900px, 1fr))"
        >
          <div>
            <h2 class="text-xl lg:text-2xl my-5 text-white">
              Hi, I'm <strong>Carina</strong>
            </h2>
            <p
              class="text-sm md:text-base lg:text-lg sm:!leading-loose md:!leading-loose lg:!leading-loose font-rubik"
            >
              I'm an aspiring Web Developer with 1 year of learning experience.
              I'm from Lisbon and I love technology and gaming.
            </p>
            <p
              class="text-sm md:text-base lg:text-lg leading-normal font-rubik sm:!leading-loose md:!leading-loose lg:!leading-loose"
            >
              My goal is to develop interactive, responsive software that
              seamlessly engages users and adapts to their needs, while
              providing invaluable functionality. Lorem ipsum dolor sit amet,
              consectetur adipisicing elit. Tempore, nostrum. Repellat, ratione.
              Rem placeat quis sequi possimus ea magni corporis?
            </p>
          </div>
          <div>
            <h2 class="text-xl lg:text-2xl my-5 text-white">
              What is my skill level?
            </h2>
            <p
              class="text-sm md:text-base lg:text-lg leading-normal font-rubik sm:!leading-loose md:!leading-loose lg:!leading-loose"
            >
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Est
              repudiandae voluptas tenetur veritatis officiis reprehenderit
              architecto iure corrupti error dolore. Lorem ipsum dolor sit, amet
              consectetur adipisicing elit. Est repudiandae voluptas tenetur
              veritatis officiis reprehenderit architecto iure corrupti error
              dolore.
            </p>
            <p
              class="text-sm md:text-base lg:text-lg leading-normal font-rubik sm:!leading-loose md:!leading-loose lg:!leading-loose"
            >
              At the moment, I am still building a solid foundation in Front-end
              development.
            </p>
          </div>
        </div>
        <h3 class="text-xl lg:text-2xl my-5 text-white">
          My current tech stack:
        </h3>
        <div
          class="flex flex-wrap md:w-full lg:mt-12 lg:grid lg:text-center lg:justify-center lg:w-full"
          style="row-gap: 70px; grid-template-columns: 300px 300px 300px"
        >
          <img class="h-10 lg:h-16 flex mx-auto" src="../assets/html-5.png" />

          <img class="h-10 lg:h-16 flex mx-auto" src="../assets/css-3.png" />

          <img class="h-10 lg:h-16 flex mx-auto" src="../assets/tailwind.png" />

          <img class="h-10 lg:h-16 flex mx-auto" src="../assets/js.png" />

          <img class="h-10 lg:h-16 flex mx-auto" src="../assets/vue.png" />

          <img class="h-10 lg:h-16 flex mx-auto" src="../assets/nuxt.png" />
        </div>
      </div>
    </main>
  </body>
</template>

<script>
export default {
  mounted() {
    document.body.classList.remove("gradient-body");
  },
};
</script>