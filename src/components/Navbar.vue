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
  <nav class="h-20 flex justify-between text-center items-center gap-5 bg-blue-900 px-10">
    <div></div>
    <div class="flex justify-between gap-3">
      <button class="text-white bg-black py-2 px-4 rounded-md cursor-pointer hover:scale-110 font-semibold text-white duration-700 hover:text-black hover:bg-white delay-100" type="button" @click="nav('Home')">Home</button>
      <button class="text-white bg-black py-2 px-4 rounded-md cursor-pointer hover:scale-110 font-semibold text-white duration-700 hover:text-black hover:bg-white delay-100" type="button" @click="nav('Students')">Students</button>
      <button class="text-white bg-black py-2 px-4 rounded-md cursor-pointer hover:scale-110 font-semibold text-white duration-700 hover:text-black hover:bg-white delay-100" type="button" @click="">User</button>
      <button class="text-white bg-black py-2 px-4 rounded-md cursor-pointer hover:scale-110 font-semibold text-white duration-700 hover:text-black hover:bg-white delay-100" type="button" @click="">Report</button>
    </div>
      <div class="space-x-5">
        <button class="text-white bg-black py-2 px-4 rounded-md cursor-pointer hover:scale-110 font-semibold text-white duration-700 hover:text-black hover:bg-white delay-100" type="button" @click="">Login</button>
      </div>
  </nav>
</template>
