<template>
  <div class="card" :key="title">
    <h3>{{ title }}</h3>
    <button @click="open" class="btn">
      {{ this.isNewsOpen ? 'Закрыть' : 'Открыть'}}
    </button>
    <p v-if="this.isNewsOpen">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi aperiam atque aut dignissimos officiis perspiciatis possimus sapiente totam ullam veniam.</p>
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
      default: false,
      validator(value) {
        return value === true || value === false
      }
    },
  },
  data () {
    return {
      isNewsOpen: this.isOpen
    }
  },
  methods: {
    open() {
      this.isNewsOpen = !this.isNewsOpen
      if (this.isNewsOpen) {
        this.$emit('open-news')
      }
    }
  }
}
</script>
