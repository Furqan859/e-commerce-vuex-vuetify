<template>
<v-container>
    <v-row class="text-center">
        <v-app>
            <v-main>
                <v-container fluid>
                      <Header />
                             <SideBar />
                               <router-view>
                                  <CardData />
                               </router-view>
                            <Footer />
                    </v-container>
                </v-main>
            </v-app>
    </v-row>
</v-container>
</template>

<script>
import Header from './Header.vue';
import Footer from './Footer.vue';
import SideBar from './SideBar.vue';
import CardData from './CardData.vue'
// import About from './About.vue'
export default {
    name: 'MainContent',
    components: {
        Header,
        Footer,
        SideBar,
        CardData
        // About
    },
    data() {
        return {

        }
    }

}
</script>
