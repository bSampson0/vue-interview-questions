<template>
  <div>
    <v-row>
      <v-col>
        <h2>Question 1: Counter</h2>
        <p>Here is a simple counter.</p>
        <v-btn @click="increment">Increment Counter</v-btn>
        <p>{{ counter }}</p>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    increment() {
      this.counter = this.counter + 1;
    },
  },
};
</script>

<style lang="scss" scoped></style>
