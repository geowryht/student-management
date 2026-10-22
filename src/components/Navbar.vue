<script>
export default {
  emits: ['go-home', 'showloginmodal'],
  data() {
    return {}
  },
  methods: {
    nav(page) {
      this.$emit('go-home', page)

    },
    openModal(i){
      this.$emit('showloginmodal', i);
    }
  }
}
</script>

<template>
  <nav class="h-20 flex justify-between text-center items-center gap-5 bg-blue-900 px-20">
    <div></div>
    <div></div>
    <div class="flex justify-between gap-3">
      <button class="text-white bg-black py-2 px-4 rounded-md cursor-pointer hover:scale-110 font-semibold text-white duration-700 hover:text-black hover:bg-white delay-100" type="button" @click="nav('Home')">Home</button>
      <button class="text-white bg-black py-2 px-4 rounded-md cursor-pointer hover:scale-110 font-semibold text-white duration-700 hover:text-black hover:bg-white delay-100" type="button" @click="nav('Students')">Students</button>
    </div>
      <div class="space-x-5">
        <button class="text-white bg-black py-2 px-4 rounded-md cursor-pointer hover:scale-110 font-semibold text-white duration-700 hover:text-black hover:bg-white delay-100" type="button" @click="nav('Home')">Report</button>
        <button class="text-white bg-black py-2 px-4 rounded-md cursor-pointer hover:scale-110 font-semibold text-white duration-700 hover:text-black hover:bg-white delay-100" type="button" @click="nav('Students')">User</button>
        <button  class="text-white bg-black py-2 px-4 rounded-md cursor-pointer hover:scale-110 font-semibold text-white duration-700 hover:text-black hover:bg-white delay-100" type="button" @click="openModal(true )">Login</button>
      </div>
  </nav>
</template>
