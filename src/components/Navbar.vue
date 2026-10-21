<script>
export default {
  emits: ['go-home'],
  data() {
    return {}
  },
  methods: {
    nav(page) {
      this.$emit('go-home', page)
    }
  }
}
</script>

<template>
  <nav class="navbar">
    <button type="button" @click="nav('Home')">Home</button>
    <button type="button" @click="nav('Students')">Students</button>
  </nav>
</template>
