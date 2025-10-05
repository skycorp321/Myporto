<template>
  <div>
    <router-view></router-view>
    <switcher />
    <Footer />
  </div>
</template>

<script>
import switcher from './components/Switcher.vue';
import Footer from '@/components/footer.vue'

export default {
  name: 'App',
  components: {
    switcher,
    Footer
  }
}
</script>

<style>

</style>
./components/Switcher.vue