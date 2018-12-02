<template>
  <div>
    <TaskFilter @update:filterString='onFilter' />
    <ul class="task-list" v-for="task in filteredTasks" :key='task.id'>
      <Task :task='task.name' />
    </ul>
  </div>
</template>

<script>
  import Task from './Task';
  import TaskModel from '../../../models/task';
  import TaskFilter from './TaskFilter';

  export default { 
    name: "TaskList",
    components: {
      Task,
      TaskFilter,
    },
    data: function data() {
      return {
        tasks: [...Array(3).keys()].map(id => new TaskModel({id, name: `Task ${id + 1}` })),
        filterString: '',
      };
    },
    computed: {
      filteredTasks: function getFilteredTasks() {
        if (this.filterString.trim() === '') {
          return this.tasks;
        }

        return this.tasks.filter(task => task.name ? task.name.includes(this.filterString) : true);
      },
    },
    methods: {
      onFilter: function onFilter(filterString) {
        this.filterString = filterString;
      }
    }
  }
  </script>

<style scoped lang="scss">

  .task-list {
    margin: 0;
    padding: 0;
    background: white;
  }

</style>
