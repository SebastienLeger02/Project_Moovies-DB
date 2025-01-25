<template>
  <div class="card bg-[#ffffff45] rounded-2xl" >
    <img class="card-img-top max-h-[300px]" :src="movie.img" />
    <div class="card-body min-h-[130px]">
      <h4 class="card-title text-xl font-semibold">{{ movie.title }}</h4>
      <p class="card-text">{{ movie.year }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["movie"],
};
</script>

<style></style>
