<template>
  <v-content>
    <v-container fluid>
      <v-layout column>
        <v-flex xs12 class="pt-3">
          <div class="result-container">
            <v-layout row justify-center align-center fill-height>
              <v-flex xs8>
                <v-card class="tasks">
                  <TaskListHeader />
                  <TaskList />
                </v-card>
              </v-flex>
            </v-layout>
          </div>
        </v-flex>
      </v-layout>
    </v-container>
  </v-content>
</template>

<script>
import TaskListHeader from './TaskListHeader';
import TaskList from './TaskList';

  export default { 
    name: "Tasks",
    components: {
      TaskListHeader,
      TaskList,
    }
  }
  </script>

<style scoped lang="scss">
  .result-container {
    height: 100%;
  }
</style>
