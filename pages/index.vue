<template>
  <div>
    <app-loading :loading="show"></app-loading>
    <app-header></app-header>
  </div>
</template>

<script>
import AppLoading from '../components/shared/AppLoading.vue'
import AppHeader from '../components/shared/AppHeader.vue'

export default {
  components: {
    AppLoading,
    AppHeader,
  },
  data() {
    return {
      show: false,
      timeOut: 2000,
    }
  },
  mounted() {
    this.showMe()
  },
  methods: {
    showMe() {
      this.show = true
      setTimeout(() => {
        this.show = false
      }, this.timeOut)
    },
  },
}
</script>
