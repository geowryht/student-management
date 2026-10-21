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
      page: 'Home'
    }
  },
  methods: {
    showHome(i) {
      this.page = i;
    },
  }
}
</script>

<template>
  <Navbar @go-home="showHome" />
  <AddModal />
  <Home v-if="page === 'Home'" />
  <Students v-if="page === 'Students'" />
  <Footer />
</template>
