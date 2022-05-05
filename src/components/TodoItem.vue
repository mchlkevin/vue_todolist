<template>
  <div class="todo-item" :class="{ 'is-complete': todo.completed }">
    <p>
      <input type="checkbox" @change="markCompleted" style="float:left"/>
      {{ todo.title }}
      <button class="del" @click="$emit('del-todo', todo.id)">x</button>
    </p>
  </div>
</template>

<script>
export default {
  name: "todo-item",
  props: ["todo"],
  emits: ["update:completed", "del-todo"],
  methods: {
    markCompleted() {
      this.$emit("update:completed", !this.todo.completed);
    },
  },
};
</script>

<style scoped>
.todo-item {
  background: #f4f4f4;
  padding: 10px;
  border-bottom: 1px #ccc dotted;
  font-size: 20px;
}
.is-complete {
  text-decoration: line-through;
  color: red;
}
.del {
  background: #ff0000;
  height: 25px;
  width: 30px;
  border-radius: 10px;
  color: #fff;
  float: right;
}
</style>
