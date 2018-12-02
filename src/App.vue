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

  .navbar {
    background-color: #f1faf6;

    .v-btn {
      color: #777;
      background-color: transparent;
      cursor: pointer;

      &.active {
        color: #555;
        background-color: #e7e7e7;
        cursor: pointer;
      }

      &:hover {
        color: #333;
        background-color: #92e7bf;
      }
    }

    .username {
      label {
        font-weight: normal;
        margin-right: 10px;
      }

      input {
        border: 1px inset lightgreen;
        width: 200px;
        padding: 3px;
        text-align: center;
      }
    }
  }

  .result-container {
    height: 100%;
  }

  .task-list-header {
    position: relative;
    padding: 1px 1px 1px 10px;
    background: linear-gradient(to bottom, #41B683, #88D4B3 100%);
    border-bottom: #41B683 solid 2px;
  }

  .task-list {
    margin: 0;
    padding: 0;
    background: white;
  }

  .task-item {
    position: relative;
    box-sizing: content-box;
    padding: 15px;
    height: 22px;
    list-style: none;
    background-color: white;
    border-bottom: #41B683 solid 1px;
  }

</style>
