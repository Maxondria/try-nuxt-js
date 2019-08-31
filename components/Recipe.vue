<template>
  <nuxt-link :to="`/recipes/${id}`">
    <article class="recipe">
      <div class="thumbnail" :style="{ backgroundImage: `url(${thumbnail})`}"></div>
      <h1>{{title}}</h1>
      <p>{{previewText}}</p>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  props: ["thumbnail", "title", "previewText", "id"]
};
</script>

<style scoped>
.recipe {
  box-sizing: border-box;
  width: 280px;
  margin: 8px;
  padding: 8px;
  border: 1px solid #cccccc;
  box-shadow: 0 2px 2px #eeeeee;
}

a {
  text-decoration: none;
  color: black;
}

.thumbnail {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 200px;
  margin-bottom: 10px;
}
</style>