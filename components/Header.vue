<template>
  <nav class="bg-white w-full">
    <div class="flex py-3 justify-between items-center">
      <span
        class="antialiased font-comfortaa text-3xl text-gray-900 hover:opacity-50 cursor-pointer"
        >mértz
      </span>
      <div>
        <a
          href="#"
          class="text-sm px-3 py-2 leading-none border rounded text-gray-900 border-gray-900 hover:border-transparent hover:text-white hover:bg-gray-600 mt-4 lg:mt-0"
          >Shop Now</a
        >
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      toggle: false,
    }
  },
}
</script>

<style>
.font-comfortaa {
  font-family: 'Comfortaa', cursive;
}
</style>
