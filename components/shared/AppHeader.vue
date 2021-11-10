<template>
  <header class="relative w-screen h-screen bg-green-600">
    <div class="text-3xl font-bold text-gray-300">
      <div class="absolute left-10 top-10">
        <div class="w-10 h-2 mb-2 bg-gray-300 rounded-md"></div>
        <p>MERRY</p>
        <p>CHRISTMAS</p>
      </div>
      <div class="absolute left-10 bottom-10">
        <p>test</p>
        <p>test</p>
      </div>
    </div>
    <div
      class="absolute w-1/3 bg-gray-300 rounded-lg top-2/4 left-2/4"
      style="transform: translate(-50%, -50%); height: calc(100vh - 80px)"
    ></div>
    <div class="text-3xl font-bold text-gray-300">
      <div class="absolute right-10 top-10">
        <p>24</p>
      </div>
      <div class="absolute right-10 bottom-10">
        <p>test</p>
        <p>test</p>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'app-header',
}
</script>
