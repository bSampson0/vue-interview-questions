<template>
  <div id="home">
    <v-container>
      <v-row>
        <v-col>
          <h1>This is your coding interview test environment.</h1>
          <p>Complete the following questions.</p>
          <ul>
            <li>Question 1: Create a simple counter.</li>
            <li>Question 2: Display json data on the screen.</li>
            <li>Question 3: Show sample data in a component.</li>
          </ul>
        </v-col>
      </v-row>
      <v-divider class="mt-4 mb-4"></v-divider>
      <Counter />
      <v-divider class="mt-4 mb-4"></v-divider>
      <APITest />
      <v-divider class="mt-4 mb-4"></v-divider>
      <ShowData />
    </v-container>
  </div>
</template>

<script>
import Counter from "@/components/Counter.vue";
import APITest from "@/components/APITest.vue";
import ShowData from "@/components/ShowData.vue";
export default {
  name: "Home",
  components: { Counter, APITest, ShowData },
};
</script>
