<template>
  <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div>
      <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title" />
    </div>
    <p>{{ recipe.descriptionText }}</p>
  </section>
</template>

<script>
export default {
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipe: [
            {
              id: "1",
              title: "Delicious Burger",
              previewText: "Awesome Burger!",
              descriptionText: "This is really a delicious meal!",
              thumbnail:
                "https://i2.wp.com/innovation-village.com/wp-content/uploads/2020/09/food-supply-network.jpg?fit=768%2C461&ssl=1"
            },
            {
              id: "2",
              title: "Delicious Fish",
              previewText: "Awesome Fish!",
              descriptionText: "This is really a delicious meal!",
              thumbnail:
                "https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/20190503-delish-pineapple-baked-salmon-horizontal-ehg-450-1557771120.jpg"
            }
          ].find(el => el.id === context.params.id)
        });
      }, 1500);
    });
  }
};
</script>

<style scoped>
.single-recipe {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
}

.recipe-image {
  width: 100%;
}
</style>
