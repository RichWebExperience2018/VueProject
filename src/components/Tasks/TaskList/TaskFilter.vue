<template>
  <v-layout row justify-space-between align-center class="task-filter-container">
      <input type="text" placeholder="Type here to filter Tasks" v-model="filterString" />
      <button class="clear-filter-button" @click="onClear">Clear</button>
  </v-layout>
</template>

<script>
  export default {
    name: "TaskFilter",
    data() {
      return {
        filterString: ''
      }
    },
    watch: {
      filterString(newFilterString){
        this.$emit('update:filterString', newFilterString);
      }
    },
    methods: {
      onClear(){
        this.filterString = '';
      }
    }
  }
</script>

<style scoped lang="scss">

  .task-filter-container {
    border: 2px inset rgba(24, 69, 49, 0.46);
    height: 40px;
  }

  input {
    padding: 1px 5px;
    margin: 1px 10px;
    flex: auto;
    border: inherit;
    border-style: inset;
  }

  button {
    margin-left: 10px;
    margin-right: 10px;
    padding: 1px 5px;
    border: inherit;
    border-radius: 2px;
    background-color: #96cfb0;
  }

</style>
