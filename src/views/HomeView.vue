<template>
  <div>
    <template-view>
      <div class="container">
        <h1>This is my HomeView Page</h1>
      </div>
    </template-view>
  </div>
</template>

<script>
import TemplateView from './TemplateView.vue'

export default {
  components: { TemplateView },
  name: 'HomeView',
}
</script>

<style scoped>

</style>