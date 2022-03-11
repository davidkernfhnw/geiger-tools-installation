<template>
<v-container fluid>
  <v-row no-gutters class="d-flex justify-center">
    <v-tabs class="d-flex justify-center pb-10" v-model="tab" align-with-title fixed-tabs>
      <v-tab><v-icon class="pr-3">mdi-android</v-icon>Android</v-tab>
      <v-tab><v-icon class="pr-3">mdi-microsoft</v-icon>Microsoft</v-tab>
      <v-tab><v-icon class="pr-3">mdi-apple</v-icon>Apple</v-tab>
      <v-tab><v-icon class="pr-3">mdi-linux</v-icon>Linux</v-tab>
    </v-tabs>
    <v-tab-items v-model="tab">
      <v-tab-item>
        
      </v-tab-item>
    </v-tab-items>
  </v-row>
  <InstructionSteps></InstructionSteps>
  </v-container>
</template>s


<script>
import InstructionSteps from '../components/InstructionSteps.vue'
export default {
  name: "InstructionView",
  components: {
    InstructionSteps
    
  },
  data() {
    return {
      tab: null,
    };
  },
};
</script>

<style>
</style>
