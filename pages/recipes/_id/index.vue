<template>
  <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div>
      <img class="recipe-image" :src="recipe.thumbnail" />
    </div>
    <p>{{recipe.previewText}}</p>
  </section>
</template>

<script>
export default {
  asyncData(context) {
    return new Promise(resolve => {
      setTimeout(() => {
        resolve({
          recipe: [
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
          ].find(recp => recp.id === context.params.id)
        });
      }, 1500);
    });
  }
};
</script>

<style>
.single-recipe {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
  flex-direction: column;
}

.recipe-image {
  width: 60%;
  height: 600px;
}
</style>