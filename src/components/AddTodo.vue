<template>
  <div>
    <form @submit="addTodo">
      <input type="text" v-model="title" name="title" placeholder="Add Todo" />
      <input type="submit" class="btn" value="Add Todo" />
    </form>
  </div>
</template>

<script>
export default {
  name: "AddTodo",
  data() {
    return {
      title: "",
    };
  },
  methods: {
    addTodo(e) {
      e.preventDefault();
      const newTodo = {
        title: this.title,
        completed: false,
      };
      //   send to parent
      this.$emit("add-todo", newTodo);
      this.title = "";
    },
  },
};
</script>

<style scoped></style>
