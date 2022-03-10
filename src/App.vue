<template>
  <v-app>
    <v-app-bar fixed app>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-app-bar-title>
        <img
          src=".//assets/geiger_logo.png"
          alt="logo"
          class="logo pr-4"
          width="120"
        />
      </v-app-bar-title>
      <v-app-bar-title>Tools Installation</v-app-bar-title>
    </v-app-bar>
    <v-main>
      
        <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({
    //
  }),
};
</script>

<style scoped>
.logo {
  padding-top: 15px;
}
</style>
