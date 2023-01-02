<template>
    <v-app>
        <v-navigation-drawer app expand-on-hover>
        <v-list dense nav>
          <v-list-item v-for="item in items" :key="item.title" link>
           
            <v-list-item-content>
              <v-list-item-title>
                <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
                {{ item.title }}
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
    </v-navigation-drawer>
    </v-app>
  </template>
  
  <script>
  export default {
    name: 'App',
    data: () => ({
      items: [
        { title: 'Dashboard', icon: 'mdi-view-dashboard' },
        { title: 'Account', icon: 'mdi-account-box' },
        { title: 'Settings', icon: 'mdi-cog' },
      ],
    }),
  };
  </script>