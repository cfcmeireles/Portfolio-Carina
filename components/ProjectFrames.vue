<template>
  <div class="project-frames">
    <h2><slot name="title"></slot></h2>
    <slot name="image"></slot>
    <p><slot name="description"></slot></p>
    <div class="skills-bar">
      <p>Skills used:</p>
      <slot name="skills"></slot>
    </div>
  </div>
</template>

<style scoped>
@media only screen and (max-width: 1650px) {
  .project-frames {
    margin-bottom: 20px;
  }
}

@media only screen and (min-width: 1650px) {
  .project-frames:hover {
    transform: scale(1.1);
    transition: ease-in-out 0.5s;
    box-shadow: 0 3px 3px rgba(0, 0, 0, 0.2);
  }
}
/* img {
  height: 300px;
  width: 100%;
} */

.project-frames {
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
/* .project:hover,
.project-2:hover {
  margin-top: 40px;
} */

.project-frames p {
  color: black;
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
</style>