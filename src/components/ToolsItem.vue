<template>
  <v-card class="mx-5 my-5" max-width="344" min-width="300">
    <v-img :src="require('@/assets/' + image + '')" height="250px"></v-img>
    <v-card-subtitle>
      <v-icon class="px-2" :color="getColor(android)">mdi-android</v-icon>
      <v-icon class="px-2" :color="getColor(microsoft)">mdi-microsoft</v-icon>
      <!-- <v-icon class="px-2" :color="getColor(apple)">mdi-apple</v-icon>
      <v-icon class="px-2" :color="getColor(linux)">mdi-linux</v-icon> -->
    </v-card-subtitle>

    <v-card-title> {{title}} </v-card-title>

    <v-card-actions>
      <v-btn color="green dark-2" text @click="getInstructions()"> {{btnText}} </v-btn>
      <v-spacer></v-spacer>

      <!-- <v-btn icon @click="show = !show">
        <v-icon>{{ show ? "mdi-chevron-up" : "mdi-chevron-down" }}</v-icon>
      </v-btn> -->
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
          I'm a thing. But, like most politicians, he promised more than he
          could deliver. You won't have time for sleeping, soldier, not with all
          the bed making you'll be doing. Then we'll go with that data file!
          Hey, you add a one and two zeros to that or we walk! You're going to
          do his laundry? I've got to find a way to escape.
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
export default {
  name: "ToolsItem",
  data: () => ({
    show: false,
  }),
  props: {
    title: String,
    android: Boolean,
    apple: Boolean,
    microsoft: Boolean,
    linux: Boolean,
    image: String,
    btnText: String,
    btnClicked: Function,
  },
  methods: {
     getColor(isAvailable){
      if(isAvailable){
        return "blue";
      }
      else {
        return "grey lighten-2";
      }
    },
    getInstructions(){
      this.$router.push({name: 'instructions'})
    },
     
  }
};
</script>

<style scoped>
</style>