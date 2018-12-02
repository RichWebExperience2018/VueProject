<template>
    <li class="task-item">
      <span class="text">{{ task }}</span>
    </li>
</template>

<script>
  export default { 
    name: "Task",
    props: {
      task: {
        type: String,
        default: 'Task X',
      },
    },
  }
  </script>

<style scoped lang="scss">
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
