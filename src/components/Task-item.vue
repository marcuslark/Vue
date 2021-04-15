<!-- Added the list of items here -->
<!-- To pass data from child to parent compontent we use
@emit method using click event -->
<template>
  <li>
    <button @click.self="$emit('complete')" :class="className">
      <i class="far fa-circle"></i> {{ task.title }}
    </button> 
    <button @click="$emit('remove')"><i class="far fa-trash-alt"></i></button>
  </li>
</template>

<!-- Added props to pass data from parent to child
component -->
<script>
export default {
  name: "TaskItem",
  props: ["task"],
  computed: {
    className() {
      let classes = ['toggle'];
      if(this.task.completed) {
        classes.push('toggle-completed');
      }
      return classes.join(' ');
    }
  }
};
</script>
