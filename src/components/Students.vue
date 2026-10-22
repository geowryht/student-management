<script>
export default {
  emits: ['open'],
  data() {
    return {

    }
  },
  methods: {
    addBtn() {
      this.$emit('open', true);
    },

  }
}

</script>

<template>
  <main class="w-full h-screen px-10 py-2 space-y-2 mt-2">

    <div class="flex justify-end px-5 w-full">
      <button @click="addBtn" class="px-5 py-3 bg-slate-600 text-white text-center rounded-lg hover:bg-slate-400 
        hover:text-black hover:scale-105 duration-300 hover:font-semibold cursor-pointer">+
        Add</button>
    </div>
    <div class="space-y-2">

      <div class="w-full h-fit min-h-20 p-5 border flex justify-between items-center bg-gray-50 shadow-xl rounded-lg">
        <div class="">
          <p class="font-bold text-lg">Name</p>
          <p class="font-semibold text-gray-800/70 text-md">Jieu Pandian</p>
        </div>
        <div class="text-center">
          <p class="font-bold text-lg">Age</p>
          <p class="font-semibold text-gray-800/70 text-md">22 </p>
        </div>
        <div class="text-center">
          <p class="font-bold text-lg">Address</p>
          <p class="font-semibold text-gray-800/70 text-md">Tagum City</p>
        </div>
        <div class="text-center">
          <p class="font-bold text-lg">Contact</p>
          <p class="font-semibold text-gray-800/70 text-md">09654784374</p>
        </div>
        <div class="text-center">
          <p class="font-bold text-lg">Status</p>
          <p class="font-semibold text-gray-800/70 text-md">Present</p>
        </div>
        <div class="space-x-2">
          <button class="px-5 py-2 bg bg-green-600 text-gray-50 font-semibold rounded-md  hover:bg-green-400 
        hover:text-black hover:scale-105 duration-300 hover:font-semibold cursor-pointer">Edit</button>
          <button class="px-5 py-2 bg bg-red-600 text-gray-50 font-semibold rounded-md  hover:bg-red-400 
        hover:text-black hover:scale-105 duration-300 hover:font-semibold cursor-pointer">Delete</button>
        </div>
      </div>
      
    </div>
  </main>
</template>
