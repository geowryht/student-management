<script>
import Footer from './components/Footer.vue'
import Home from './components/Home.vue'
import Navbar from './components/Navbar.vue'
import Students from './components/Students.vue'
import AddModal from './components/AddModal.vue'
import LoginModal from './components/LoginModal.vue'

export default {
  name: 'App',
  components: {
    Footer, Home, Navbar, Students, AddModal, LoginModal,
  },
  data() {
    return {
      listsOfStudents: [{ no: 1, name: 'Crystal Marise Filamen', age: 22, address: 'Prk. Pagkakaisa Pagsabangan', contact: '0924 538 9549', status: 'Present' },
      { no: 2, name: 'Angel Clarido', age: 25, address: 'Monkayo, Davao De Oro', contact: '0927 806 4315', status: 'Present' },],

      listsOfGuardian: [{ no: 1, name: '', age: 0, address: '', contact: '', },
      { no: 1, name: '', age: 0, address: '', contact: '', },],

      page: 'Home',
      addStudents: false,
      login: false,
    }
  },
  methods: {
    showHome(i) {
      this.page = i;
    },

    showModal(a) {
      this.addStudents = a;
    },
    openloginmodal(i) {
      this.login = i
    },
    closeModal(i) {
      this.login = i;
    },
  }
}
</script>

<template>
  <Navbar @go-home="showHome" @showloginmodal="openloginmodal" />
  <AddModal v-if="addStudents" />
  <Home v-if="page === 'Home'" :studentHome="listsOfStudents" />
  <Students v-if="page === 'Students'" @open="showModal" />
  <LoginModal v-if="login === true" @close="closeModal" />
  <Footer />
</template>
