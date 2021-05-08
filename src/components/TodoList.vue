<template>
  <div class="home" v-if="this.todos">
    <div v-for="todo in this.todos" v-bind:key="todo.id">
        <TodoItem :todo="todo" @deleteTodo="deleteTodo"></TodoItem>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TodoItem from './TodoItem.vue'
import addTodo from './addTodo.vue'

export default defineComponent({
  name: "TodoList",
  data() {
      return {
          todos: [
              {
                  id: 1,
                  text: "First Todo",
                  completed: false
              }
          ]
      }
  },
  methods: {
      deleteTodo: function(id: number) {
         let newTodos = this.todos.filter(todo => todo.id != id)
         this.todos = newTodos
      }
  },
  components: {
      TodoItem
  },
});
</script>
