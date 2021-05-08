<template>
  <div>
    <TodoList></TodoList>
  </div>
</template>

<script lang="ts">

import TodoList from "@/components/TodoList.vue"

  export default {
    name: "Todo",
    components: {
      TodoList
    }
  }
</script>