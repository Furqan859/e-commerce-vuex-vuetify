<template>
<v-container>
    <v-row class="text-center">
        <v-app>

            <!-- App.vue -->

            <v-app>

                <!-- Sizes your content based upon application components -->
                <v-main>

                    <!-- Provides the application the proper gutter -->
                    <v-container fluid>
                        <!-- If using vue-router -->
                        <Header />
                        <SideBar />
                        <router-view>

                        </router-view>
                        <Footer />
                    </v-container>

                </v-main>

            </v-app>

            <v-main>
                <router-view />
            </v-main>
            <Footer />
        </v-app>

    </v-row>
</v-container>
</template>

<script>
import Header from './Header.vue';
import Footer from './Footer.vue';
import SideBar from './SideBar.vue';
// import About from './About.vue'
export default {
    name: 'MainContent',
    components: {
        Header,
        Footer,
        SideBar,
        // About
    },
    data() {
        return {

        }
    }

}
</script>
