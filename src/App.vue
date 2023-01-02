<template>
<v-app>

    <!-- App.vue -->

    <v-app>
       

        <!-- Sizes your content based upon application components -->
        <v-main>

            <!-- Provides the application the proper gutter -->
            <v-container fluid>
                <!-- If using vue-router -->
                <router-view></router-view>
            </v-container>
        </v-main>

    </v-app>

    <v-main>
        <router-view />
    </v-main>
    <Footer />
</v-app>
</template>

<script>
// import Header from './components/Header.vue';
// import Footer from './components/Footer.vue';
// import SideBar from './components/SideBar.vue';
export default {
    name: 'App',
    components: {
       
    },

    data: () => ({
        //
    }),
};
</script>
