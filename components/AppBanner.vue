<template>
  <section class="min-h-screen flex flex-col justify-center relative px-44">
    <div
      class="max-w-7xl flex flex-col justify-center items-center text-center lg:text-left lg:items-start h-full"
    >
      <h1 class="font-semibold text-5xl">Wear it like you mean it.</h1>
      <p class="max-w-lg my-4">
        Everything made out of quality materials for creative enthusiast
        supporting technology at large.
      </p>
      <nuxt-link
        to="/"
        class="
        transition
          px-16
          py-4
          font-semibold
          border-2 border-black
          ease-in-out delay-150
          hover:text-white hover:bg-black
          ease-in-out duration-300
        "
      >
        Shop Now
      </nuxt-link>
      <div class="benefits my-4 text-sm flex gap-x-6">
        <span>Free Signup</span>
        <span>No charges</span>
        <span>Over 100+ designs</span>
      </div>
      <div class="categories flex divide-x-2 divide-black absolute bottom-6">
        <span class="text-xs pr-10">Men</span>
        <span class="text-xs px-10">Women</span>
        <span class="text-xs px-10">Kids</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
    name: "AppBanner",
}
</script>

<style scoped>
section {
  background-image: url('~/assets/images/banner_bg.png');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: right;
}

a {
  transition: 500ms;
}

.categories span {
  @apply
	    text-xs;
}
</style>