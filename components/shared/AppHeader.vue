<template>
  <header
    id="up"
    class="relative h-screen bg-fixed bg-center bg-no-repeat bg-cover"
    :style="{ backgroundImage: `url(${backgroundUrl})` }"
  >
    <div
      class="flex items-center justify-center h-screen bg-transparent bg-opacity-50 "
      style="background: rgba(0, 0, 0, 0.5)"
    ></div>
  </header>
</template>

<script>
import backgroundUrl from '~/assets/images/christmas-background.jpg'

export default {
  name: 'app-header',
  data() {
    return {
      backgroundUrl,
    }
  },
}
</script>
