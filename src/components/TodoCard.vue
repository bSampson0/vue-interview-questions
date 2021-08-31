<template>
  <div>
    <v-card :color="completed ? 'green' : 'red'">
      <v-card-title>
        {{ title }}
      </v-card-title>
      <v-card-text> Completed: {{ completed }} </v-card-text>
      <v-card-actions>
        <v-btn @click="completed = !completed">Completed</v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: "",
    },
    completed: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="scss" scoped></style>
