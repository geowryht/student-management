<script>
import Footer from './components/Footer.vue'
import Home from './components/Home.vue'
import Navbar from './components/Navbar.vue'
import Students from './components/Students.vue'

export default {
  name: 'App',
  components: { Footer, Home, Navbar, Students },
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
  <Home v-if="page === 'Home'" />
  <Students v-if="page === 'Students'" />
  <Footer />
</template>
