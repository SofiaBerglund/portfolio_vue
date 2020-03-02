<template>
  <div class="project-container">
    <a :href="this.link">
      <div class="project-title">
        <p>{{ title }}</p>
      </div>
      <div class="project-img">
        <img :src="this.image" alt="project">
      </div>
    </a>
  </div>
</template>

<script>
export default {
  name: "Project",
  props: ["id", "title", "image", "link"]
};
</script>

<style lang="scss">
.project-container {
  width: calc(50% - 40px);
  height: auto;
  min-height: 430px;
  margin: 20px 0;
  padding: 0 10px 10px;
  border: 2px solid #f7cfd9;
  .project-img {
    height: 350px;
    overflow: hidden;
    img {
      object-fit: cover;
      width: 100%;
      height: 100%;
    }
  }
}
// @media (max-width: 1200px) {
//   .project-container {
//     width: 80%;
//   }
// }
@media (max-width: 800px) {
  .project-container {
    width: 60%;
  }
}
@media (max-width: 450px) {
  .project-container {
    width: 90%;
    height: 400px;
    .project-img {
    height: 300px;
    }
  }
}
</style>
