<template>
  <section class="recipes">
    <Recipe
      v-for="recipe in recipes"
      :key="recipe.id"
      :thumbnail="recipe.thumbnail"
      :title="recipe.title"
      :id="recipe.id"
      :previewText="recipe.previewText"
    />
  </section>
</template>

<script>
import Recipe from "@/components/Recipe";

export default {
  components: {
    Recipe
  },
  asyncData() {
    return new Promise(resolve => {
      setTimeout(() => {
        resolve({
          recipes: [
            {
              title: "Amazing Foods",
              thumbnail:
                "https://static.independent.co.uk/s3fs-public/thumbnails/image/2019/07/18/15/istock-855098134.jpg",
              id: "1",
              previewText: "We are the best in town"
            },
            {
              title: "Fav Hotel",
              thumbnail: "https://static.toiimg.com/photo/68283907.cms",
              id: "2",
              previewText: "You Ain't tasting Anywhere else"
            }
          ]
        });
      }, 1500);
    });
  }
};
</script>

<style scoped>
.recipes {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-content: center;
}
</style>