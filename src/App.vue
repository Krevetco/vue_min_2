<template>
  <div class="container pt-1">
    <div class="card">
      <h2>Актуальные новости {{ now }}</h2>
    </div>

    <app-news></app-news>
  </div>
</template>

<script>
import AppNews from './AppNews'
export default {
  data() {
    return {
      now: new Date().toLocaleDateString(),
      news: [
        'Джо победил',
        'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Obcaecati, rerum.'
      ]
    }
  },
  components: {
    'app-news' : AppNews
  }
}
</script>

<style lang="scss">

</style>
