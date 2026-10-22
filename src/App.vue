<script>
import Footer from './components/Footer.vue'
import Home from './components/Home.vue'
import Navbar from './components/Navbar.vue'
import Students from './components/Students.vue'
import AddModal from './components/AddModal.vue'
import User from './components/User.vue'
import Reports from './components/Reports.vue'

export default {
  name: 'App',
  components: {
  
    Footer, Home, Navbar, Students, AddModal, User, Reports 
  },
  data() {
    return {
       listsOfStudents: [{ no: 1, name: 'Crystal Marise Filamen', age: 22, address: 'Prk. Pagkakaisa Pagsabangan', contact: '0924 538 9549', status: 'Present' },
                        { no: 2, name: 'Angel Clarido', age: 25, address: 'Monkayo, Davao De Oro', contact: '0927 806 4315', status: 'Present' },],

      listsOfGuardian: [{no: 1 , name: '', age: 0, address: '', contact: '', },
                        {no: 1 ,  name: '', age: 0, address: '', contact: '', },],

      page: 'Home',
      addStudents: false
    }
  },
  methods: {
    showHome(i) {
      this.page = i;
    },

    showModal(a) {
      this.addStudents = a;
    }
  }
}
</script>

<template>
  <Navbar @go-home="showHome" />
  <AddModal v-if="addStudents" />
  <Home v-if="page === 'Home'" :studentHome="listsOfStudents" />
  <User v-if="page === 'user'" />


  <Students v-if="page === 'Students'" @open="showModal" :studentStudents="listsOfStudents" />

  <Reports v-if="page === 'Reports'" />
  <Footer />
</template>
