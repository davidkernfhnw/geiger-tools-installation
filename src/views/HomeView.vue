<template>
  <v-container fluid >
    <v-row class="d-flex justify-center">
      <ToolsItem
        v-for="tool in tools"
        v-bind:key="tool"
        :title="tool.name"
        :android="tool.android"
        :apple="tool.apple"
        :microsoft="tool.microsof"
        :linux="tool.linux"
        :image="tool.image"
        btnText="Get Tool"
       
      ></ToolsItem>
    </v-row>

  </v-container>
</template>

<script>
// @ is an alias to /src
import ToolsItem from "../components/ToolsItem.vue";

export default {
  name: "HomeView",
  components: {
    ToolsItem,
  },
  data: () => ({
    tools: [
      //image are located in src/assets
      // only provide file name instead of full path
      {
        name: "Tool Name",
        android: true,
        microsoft: false,
        apple: false,
        linux: false,
        image: "tool.png",
        
      },
      {
        name: "Tool Name2",
        android: false,
        microsoft: true,
        apple: false,
        linux: false,
        image: "tool.png",
      },
      {
        name: "Tool Name3",
        android: true,
        microsoft: false,
        apple: true,
        linux: false,
        image: "tool.png",
      },
      {
        name: "Tool Name4",
        android: true,
        microsoft: false,
        apple: false,
        linux: true,
        image: "tool.png",
      },
    ],
  }),
  methods: {
    
   


  },
};
</script>
