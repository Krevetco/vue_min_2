<template>
  <div class="container pt-1">
    <div class="card">
      <h2>Актуальные новости {{ now }}</h2>
    </div>

    <app-news
      :title="item.title"
      :key="item.id"
      v-for="item in news"
      :id="item.id"
    ></app-news>
  </div>
</template>

<script>
import AppNews from './AppNews'
export default {
  data() {
    return {
      now: new Date().toLocaleDateString(),
      news: [
        {
          title: 'Джо победил',
          id: 1,
          isOpen: false
        },
        {
          title: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Obcaecati, rerum.',
          id: 2,
          isOpen: false
        },

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
