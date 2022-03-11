<template>
  <v-app>
    <v-app-bar fixed app>
      <v-app-bar-nav-icon v-if="$route.name.match('instructions')" @click="goBack()"><v-icon large>mdi-arrow-left</v-icon></v-app-bar-nav-icon>
      <v-icon v-else large color="transparent">mdi-menu</v-icon>
      <v-spacer></v-spacer>
      <v-app-bar-title>
        <img
          src=".//assets/geiger_logo.png"
          alt="logo"
          class="logo pr-4"
          width="120"
        />
      </v-app-bar-title>
      <h3>Tools Installation</h3>
      <v-spacer></v-spacer>
    </v-app-bar>
    <v-main>
      
        <router-view ></router-view>
    </v-main>
    <v-footer>
      <v-row class="d-flex justify-center">
          <p class="pt-4">GEIGER Footer</p>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({
    //
  }),
  methods: {
   goBack(){
     this.$router.go(-1)
   }
  }
};
</script>

<style scoped>
.logo {
  padding-top: 15px;
}
</style>
