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
  <nav class="h-20 flex justify-center text-center items-center gap-5 bg-blue-900">
      <button class="text-white bg-black py-2 px-4 rounded-md cursor-pointer hover:scale-110 font-semibold text-white duration-700 hover:text-black hover:bg-white delay-100" type="button" @click="nav('Home')">Home</button>
      <button class="text-white bg-black py-2 px-4 rounded-md cursor-pointer hover:scale-110 font-semibold text-white duration-700 hover:text-black hover:bg-white delay-100" type="button" @click="nav('Students')">Students</button>
  </nav>
</template>
