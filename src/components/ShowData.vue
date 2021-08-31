<template>
  <div>
    <v-row>
      <v-col>
        <h2>Question 3: Show Data</h2>
        <TodoCard :title="data.title" :completed="data.completed" />
      </v-col>
    </v-row>
  </div>
</template>

<script>
import TodoCard from "@/components/TodoCard.vue";
export default {
  components: {
    TodoCard,
  },
  data() {
    return {
      data: null,
    };
  },
  created() {
    this.getData();
  },
  methods: {
    getData() {
      try {
        fetch("https://jsonplaceholder.typicode.com/todos/1")
          .then((resp) => resp.json())
          .then((data) => {
            this.data = data;
          });
      } catch (error) {
        console.log(error);
      }
    },
  },
};
</script>

<style lang="scss" scoped></style>
