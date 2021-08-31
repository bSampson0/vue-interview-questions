<template>
  <div>
    <v-row>
      <v-col>
        <h2>Questoin 2: Display Json</h2>
        <p>
          Pulling sample data from "https://jsonplaceholder.typicode.com/todos"
        </p>
        <p>
          {{ data }}
        </p>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
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
