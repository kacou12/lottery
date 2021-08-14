<template>
  <div class="col-md-8 mx-auto">
    <login></login>
  </div>
</template>

<script>
import Vue from 'vue'
import login from '@/components/forms/login.vue'
export default Vue.extend({
  components: { login },
})
</script>

<style lang="scss" scoped>
</style>