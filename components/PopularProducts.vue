<template>
  <section class="container px-44 mx-auto comp_margin">
    <header class="text-center">
      <h1>Popular Products</h1>
      <p class="my-4">
        We bring you some of our exclusive product with the craziest reaction
        from the market.
      </p>
    </header>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 justify-items-center">
      <div class="card"></div>
      <div class="card"></div>
      <div class="card"></div>
      <div class="card"></div>
      <div class="card"></div>
      <div class="card"></div>
      <div class="card"></div>
      <div class="card"></div>
    </div>
  </section>
</template>

<script>
export default {
    name: "PopularProducts",
}
</script>

<style scoped>
.card {
  @apply w-52
  h-64
  bg-gray-100
  m-4;
}
</style>