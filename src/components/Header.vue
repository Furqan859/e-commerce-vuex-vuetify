<template>
 
    <v-app-bar
        app clipped-left
      >
        <div class="d-flex  align-center">
         
        </div>
  
        <v-spacer></v-spacer>
       
       
  
        <router-link style="text-decoration: none; color: inherit;" to="/userProfile">
          <v-btn
          href=""
          target="_blank"
          text
        >
          <span class="mr-2">{{ userName }}</span>
          <v-row justify="space-around">
    <v-avatar>
      <img
        :src=image
        alt="John"
      >
    </v-avatar>
  </v-row>
        </v-btn>
        </router-link>

        <v-btn
          text
        >
          <span v-if="!$store.state.email" @click="logout"  class="mr-2">LogOut</span>
        </v-btn>
      </v-app-bar>
 
  </template>
  
  <script>
  
  export default {
    name: 'Header',
  
    data(){
      return{
        userName:'',
        image:''
      }
    },
    methods:{
      userInfo(){
      const data = JSON.parse(localStorage.getItem("userLogin"));
      console.log(data.username,"data name")
       this.userName = data.username;
       this.image = data.image;
      },

      logout(){
        localStorage.removeItem("userLogin");
        this.$router.push('/');
      }
      
    },
    created(){
      this.userInfo();
    }
   
  };
  </script>
  