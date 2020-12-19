<template>
  <section class="recipes">
    <Recipe
      thumbnail="https://i2.wp.com/innovation-village.com/wp-content/uploads/2020/09/food-supply-network.jpg?fit=768%2C461&ssl=1"
      title="Delicious Burger"
      previewText="Awesome Burger!"
    />
    <Recipe
      thumbnail="https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/20190503-delish-pineapple-baked-salmon-horizontal-ehg-450-1557771120.jpg"
      title="Delicious Fish"
      previewText="Awesome Fish!"
    />
  </section>
</template>

<script>
import Recipe from "@/components/Recipe";

export default {
  components: {
    Recipe
  }
};
</script>

<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}
</style>
