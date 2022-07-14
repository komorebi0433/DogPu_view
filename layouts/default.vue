<template>
  <div>
    <navbar />
  </div>
</template>

<script>
import navbar from '@/components/layouts/navbar'

export default {
  data() {
    return {
      test: true,
      test1: '登录'
    }
  },

  components: {
    navbar
  }
}
</script>

<style scoped>

</style>