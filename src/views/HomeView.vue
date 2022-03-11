<template>
<v-container fluid class="pa-10">
  <v-row class="d-flex justify-center">
    <ToolsItem v-for="i in 9" v-bind:key=i ></ToolsItem>
  </v-row>
</v-container>
</template>

<script>
// @ is an alias to /src
import ToolsItem from '../components/ToolsItem.vue'

export default {
  name: 'HomeView',
  components: {
    ToolsItem
  }
}
</script>
