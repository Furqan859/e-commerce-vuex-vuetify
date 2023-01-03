<template>
    <v-card
      :loading="loading"
      class="mx-auto my-12"
      max-width="374"
    >
      <template v-slot:loader="{ isActive }">
        <v-progress-linear
          :active="isActive"
          color="deep-purple"
          height="4"
          indeterminate
        ></v-progress-linear>
      </template>
      <v-window
    v-model="window"
    show-arrows
  >
    <v-window-item
      v-for="image in product.images"
      :key="image"
    >
      <v-card height="200px" class="d-flex justify-center align-center">
  
      <v-img
        cover
        height="200"
        :src="image"
      ></v-img>
    </v-card>
    </v-window-item>
  </v-window>
  
      <v-card-item>
        <v-card-title>
          <v-row
          align="center"
          class="mx-0"
        >
          <v-row>{{ product.title }}</v-row>
          <v-rating
            :model-value="3"
            color="amber"
            density="compact"
            half-increments
            readonly
            size="small"
          ></v-rating>
  
          <div class="text-grey ms-4">
            {{ product.rating }}
          </div>
        </v-row>
        </v-card-title>
  
        <v-card-subtitle>
          <span class="my-2">{{ product.brand }}</span>
  
          <v-icon
            color="error"
            icon="mdi-fire-circle"
            size="small"
          ></v-icon>
        </v-card-subtitle>
        <v-card-text>
       
  
       <div class=" text-subtitle-1">
       ${{ product.price }}
       </div>
 
       <div>{{ product.description }}</div>
     </v-card-text>
      </v-card-item>
  
      <v-card-actions>
        <v-btn
          color="deep-purple-lighten-2"
          variant="text"
          @click="AddToCart"
        >
          Add To Cart
        </v-btn>
      </v-card-actions>
    </v-card>
  </template>
  <script>
    export default {
      name:'CardData',
      props:["product"]
      ,
      data: () => ({
        loading: false,
        selection: 1,
        length: 3,
      window: 0,
      }),
  
      methods: {
        AddToCart () {
          this.loading = true
  
          setTimeout(() => (this.loading = false), 2000)
        },
      },
    }
  </script>