<template>
  <div>
    <form @submit="addTodo">
      <input type="text" name="title" placeholder="Input To-do list" v-model="title" style="text-align:center" />
      <input type="submit" value="Submit" class="btn" />
    </form>
  </div>
</template>

<script>
//import { v4 } from "uuid";

export default {
  name: "add-todo",
  data() {
    return {
      title: "",
    };
  },
  $emits: ["add-todo"],
  methods: {
    addTodo(e) {
      e.preventDefault();
      //const uuId = v4();
      const newTodo = {
        title: this.title,
        completed: false,
      };

      this.$emit("add-todo", newTodo);

      //for reset title input
      this.title = "";
    },
  },
};
</script>

<style scoped>
form {
  display: flex;
}
input[type="text"] {
  flex: 10;
  padding: 5px;
  font-size: 15px;
}
input[type="submit"] {
  font-size: 15px;
  flex: 2;
}
</style>
