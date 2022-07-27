<template>
  <section class="container mx-44 comp_margin flex flex-col-reverse items-center lg:items-center lg:flex-row justify-between">
    <div class="collections_caption text-center lg:text-left max-w-lg">
      <h1>Choose from our creative collection</h1>
      <p class="my-4">
        We have varieties of designs, we give you the best of the best.
      </p>
      <button class="transition ease-in-out delay-150
          hover:text-white hover:bg-black
          ease-in-out duration-300">Collections</button>
    </div>
    <div class="collections items-center">
      <div>
        <div class="card">
          <div class="path_wrap">
            <div class="path"></div>
          </div>
          <div class="non_path">
            <h3 class="bg-blue-300 p-5">Abstract</h3>
            <p>104+ Designs</p>
          </div>
        </div>
        <div class="card">
          <div class="path_wrap">
            <div class="path"></div>
          </div>
          <div class="non_path">
            <h3 class="bg-red-300 p-5">Social Media</h3>
            <p>390+ Designs</p>
          </div>
        </div>
      </div>
      <div>
        <div class="card">
          <div class="path_wrap">
            <div class="path"></div>
          </div>
          <div class="non_path">
            <h3 class="bg-green-300 p-5">Software</h3>
            <p>111+ Designs</p>
          </div>
        </div>
        <div class="card">
          <div class="path_wrap">
            <div class="path"></div>
          </div>
          <div class="non_path">
            <h3 class="bg-gray-400 p-5">Programming</h3>
            <p>70+ Designs</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
    name: "CategorySection",
}
</script>

<style scoped>
.collections > div {
  @apply flex
  gap-x-12
  mb-6;
}

.card {
  @apply bg-white
      relative
      w-44
      h-44
      shadow-xl
      rounded-2xl
      mt-0;
}

.card .non_path {
  @apply flex
      absolute
      flex-col
      items-center
      justify-between
      w-full
      h-full
      p-5;

  z-index: 5;
}

.card .non_path h3 {
  @apply
        py-1
        text-sm
        text-white
        rounded-full;
}

.card .non_path p {
  @apply font-medium
          text-gray-400;
}

.card .path_wrap .path {
  @apply rounded-t-2xl;

  z-index: 1;
  width: 100%;
  height: 100%;
  position: absolute;
  background: #f9fafb;
  clip-path: circle(100% at 50% -35%);
}
</style>