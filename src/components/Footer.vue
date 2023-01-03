<template>
   <v-footer app fixed
  >
    <v-row
      justify="center"
      no-gutters
    >
     
      <v-col
        class="primary lighten-2 py-4 text-center white--text"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>E-Commerce Store</strong>
      </v-col>
    </v-row>
  
  </v-footer>
</template>

<script>
export default {
    name:'Footer',

}
</script>

<style>

</style>