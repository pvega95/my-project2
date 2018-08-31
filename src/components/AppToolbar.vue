<template>
  <v-toolbar color="red lighten-1" dark>
    <v-toolbar-side-icon></v-toolbar-side-icon>
    <v-toolbar-title>ScotiaBank</v-toolbar-title>
    <v-spacer></v-spacer>
    <div class="hidden-sm-and-down">
      <v-btn flat>GRUPO MF</v-btn>
      <v-btn flat>TRABAJA CON NOSOTROS</v-btn>
      <v-btn flat>NOSOTROS</v-btn>
      <router-link to="/login">
        <v-btn flat>INICIAR SESION</v-btn>
      </router-link>
    </div>
  </v-toolbar>
</template>
<script>
export default {

}
</script>
<style scoped>
div a {
    text-decoration: none;
    }
</style>
