<template>
  <div
    v-if="loading"
    class="fixed inset-0 flex items-center justify-center w-full h-full transition-opacity duration-300 bg-white "
    style="z-index: 6000"
  >
    <div class="flex-col">
      <img src="~/assets/images/gift.gif" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'app-loading',
  props: {
    loading: {
      type: Boolean,
      default: false,
    },
  },
}
</script>
