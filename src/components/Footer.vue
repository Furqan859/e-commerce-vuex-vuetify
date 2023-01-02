<template>
   <v-footer app
  >
    <v-row
      justify="center"
      no-gutters
    >
      <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        text
        rounded
        class="my-2"
      >
        {{ link }}
      </v-btn>
      <v-col
        class="primary lighten-2 py-4 text-center white--text"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>E-Commerce Footer</strong>
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