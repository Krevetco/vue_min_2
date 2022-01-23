<template>
  <div class="card" :key="title">
    <h3>{{ title }}</h3>
    <button @click="isOpen = !isOpen" class="btn">Открыть</button>
    <p v-if="isOpen">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi aperiam atque aut dignissimos officiis perspiciatis possimus sapiente totam ullam veniam.</p>
  </div>
</template>

<script>
export default {
  // props: {
  //   title: String,
  //   id: Number,
  //   isOpen: Boolean
  // },
  props: {
    title: {
      tyep: String,
      required: true,
    },
    id: {
      tyep: Number,
      required: true,
    },
    isOpen: {
      tyep: Boolean,
      required: false,
      default: false
    },
  },
  data () {
    return {
      //isOpen: false
    }
  }
}
</script>
