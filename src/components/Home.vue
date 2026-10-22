<script>
export default{
  props: ['studentHome'],
  data(){
    return{

    }
  },
  methods:{

  }
}
</script>

<template>

  <div class="h-screen px-10 py-5">

    <div class="py-5">
      <h1 class="font-mono text-2xl">STUDENT MANAGEMENT SYSTEM: <span class="text-xl text-gray-600">East Watch Services,
          LLC</span></h1>
    </div>

    <div class="bg-gray-200 w-full py-5 rounded-md ">

      <div class="grid grid-cols-6 flex h-full items-center text-center">

        <p class="text-gray-700 font-semibold ">No.</p>
        <p class="text-gray-700 font-semibold ">Name</p>
        <p class="text-gray-700 font-semibold ">Age</p>
        <p class="text-gray-700 font-semibold ">Address</p>
        <p class="text-gray-700 font-semibold ">Contact</p>
        <p class="text-gray-700 font-semibold ">Status</p>
      </div>

    </div>

    <div v-for="(students, index) in studentHome">

      <div class="bg-gray-50 py-5 rounded-md">
        <div class="grid grid-cols-6 h-full items-center text-center">

          <p class="font-semibold">{{ students.no }}.</p>
          <p class="font-semibold">{{ students.name }}</p>
          <p class="font-semibold">{{ students.age }}</p>
          <p class="font-semibold">{{ students.address }}</p>
          <p class="font-semibold">{{ students.contact }}</p>
          <p class="font-semibold">{{ students.status }}</p>
        </div>
      </div>

    </div>
  </div>
</template>
