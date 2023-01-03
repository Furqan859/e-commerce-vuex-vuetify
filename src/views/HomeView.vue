<template>
<v-container>

    <v-row>

        <v-app>

            <v-main>

                <v-container fluid>

                    <Header />
                    <v-layout row>
                        <card-data v-for="product in products" :key="product.id" :product="product" />
                    </v-layout>
                    <SideBar />
                    <router-view>

                    </router-view>
                    <Footer />
                </v-container>
            </v-main>
        </v-app>
    </v-row>
</v-container>
</template>

<script>
// import MainContent from '../components/MainContent'
import Header from '../components/Header.vue';
import Footer from '../components/Footer.vue';
import SideBar from '../components/SideBar.vue';
import CardData from '../components/CardData.vue'

export default {

    name: 'HomeView',

    components: {

        Header,
        Footer,
        SideBar,
        CardData

    },

    computed:{
        products(){
            return this.$store.state.products;
        }
    }
    ,
    mounted(){
         this.$store.dispatch('getProducts')
    }
}
</script>
