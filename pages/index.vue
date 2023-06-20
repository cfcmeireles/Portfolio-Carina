<template>
  <main id="home-page">
    <div class="home">
      <h1>Carina Meireles</h1>
      <h2>
        I am an aspiring developer based in Lisbon, Portugal
        <br />
        Currently employed by Miniclip
      </h2>
      <NuxtLink to="https://github.com/cfcmeireles" target="_blank">
        <img
          src="../assets/github-logo.png"
          class="github-icon"
          alt="GitHub Logo"
        />
      </NuxtLink>
      <NuxtLink
        to="https://www.linkedin.com/in/carina-meireles/"
        target="_blank"
      >
        <img
          src="../assets/linkedin-logo.png"
          class="linkedin-icon"
          alt="Linkedin Logo"
        />
      </NuxtLink>
    </div>
  </main>
</template>

<script setup>
</script>

<style scoped>
#home-page {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.home {
  text-align: center;
}

.github-icon {
  width: 3%;
  padding-right: 10px;
}
.linkedin-icon {
  width: 3%;
}
</style>