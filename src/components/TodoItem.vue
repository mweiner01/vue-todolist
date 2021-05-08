<template>
  <div class="home">
    <h1>{{ todo.text }}</h1>
    <button @click="deleteTodo(todo.id)">Delete Todo</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";


export default defineComponent({
  name: "TodoItem",
  props: {
      todo: {
          required: true
      }
  },
  methods: {
    deleteTodo: function(id: number) {
        this.$emit("deleteTodo", id)
    }
  },
  components: {
    
  },
});
</script>
