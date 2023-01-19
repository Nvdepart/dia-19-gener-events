<template>
  <v-container>
    <v-row>
      <v-col>
        <h1>Event 1</h1>
        <v-list @scroll="onListScroll">
          <v-list-item v-for="item in items" :key="item.id">{{ item.text }}</v-list-item>
        </v-list>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-btn @click="changeCircleColor" color="primary">Changez la couleur</v-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-alert :color="circleColor" width="800" height="300"></v-alert>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      circleColor: "red",
      items: [
        { id: 1, text: "Item 1" },
        { id: 2, text: "Item 2" },
        { id: 3, text: "Item 3" },
        { id: 4, text: "Item 4" },
        { id: 5, text: "Item 5" },
        { id: 6, text: "Item 6" },
        { id: 7, text: "Item 7" },
        { id: 8, text: "Item 8" },
        { id: 9, text: "Item 9" },
        { id: 11, text: "Item 11" },
        { id: 10, text: "Item 10" },
        { id: 12, text: "Item 12" },
        { id: 13, text: "Item 13" },
        { id: 14, text: "Item 14" },
        { id: 15, text: "Item 15" },
        { id: 16, text: "Item 16" },
        { id: 17, text: "Item 17" },
        { id: 18, text: "Item 18" },
        { id: 19, text: "Item 19" },
      ]
    }
  },
  methods: {
    changeCircleColor() {
      this.circleColor = this.circleColor === "red" ? "blue" : "red";
    },

    onListScroll() {
      console.log("La liste a été défilée");
    }
  }
}
</script>

<style scoped>

</style>