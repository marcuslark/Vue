<template>
  <div id="app">
    <!-- Imported child-compontent "task" -->
    <task v-bind:tasks="tasks"></task>
  </div>
</template>

<script>
import Task from "./components/Task";

export default {
  name: "App",
  components: {
    Task,
  },
  data() {
    return {
      tasks: [
        {
          id: 1,
          title: "Call bank",
          completed: true,
        },
        {
          id: 2,
          title: "Watch netflix",
          completed: true,
        },
        {
          id: 3,
          title: "Go shopping",
          completed: false,
        },
        {
          id: 4,
          title: "Learn Drums",
          completed: false,
        },
        {
          id: 5,
          title: "Clean House",
          completed: false,
        },
      ],
    };
  },
};
</script>