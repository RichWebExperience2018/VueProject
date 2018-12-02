<template>
  <v-app>
    <Navbar />
    <Tasks />
    <Footer />
  </v-app>
</template>

<script>
 import Footer from './components/Footer';
 import Navbar from './components/Navbar';
 import Tasks from './components/Tasks';

  export default { 
    components: {
      Footer,
      Navbar,
      Tasks,
    }
  }
</script>

<style scoped lang="scss">

  button, input, select, textarea {
    border-style: inherit;
  }

</style>
