<script>
import Footer from './components/Footer.vue'
import Home from './components/Home.vue'
import Navbar from './components/Navbar.vue'
import Students from './components/Students.vue'
import AddModal from './components/AddModal.vue'

export default {
  name: 'App',
  components: {
    Footer, Home, Navbar, Students, AddModal,
  },
  data() {
    return {
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
  <Home v-if="page === 'Home'" />
  <Students v-if="page === 'Students'" @open="showModal"/>
  <Footer />
</template>
