<template>
  <div class="card" :key="item">
    <h3>{{ item }}</h3>
    <button @click="isOpen = !isOpen" class="btn">Открыть</button>
    <p v-if="isOpen">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi aperiam atque aut dignissimos officiis perspiciatis possimus sapiente totam ullam veniam.</p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      item: 'item',
      isOpen: false
    }
  }
}
</script>
