<template>
  <div>

    <header>
        <topbar-component />
        <nav-bar />
        <carousel-component />

    </header>

    <main>
        <slot> </slot>
    </main>

    <footer>
        <h1>We write footer here.</h1>
    </footer>

  </div>
</template>

<script>
import NavBar from '../components/NavBar.vue'
import TopbarComponent from '@/components/TopbarComponent.vue'
import CarouselComponent from '@/components/CarouselComponent.vue'

export default {
  name: 'TemplateView',
  components: {NavBar,TopbarComponent, CarouselComponent}
}
</script>

<style scoped>

</style>