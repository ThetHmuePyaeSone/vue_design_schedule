<template>
    <div class="header">
        <img class="vector" src="../assets/img/wilkinson_logo.png" />
        <img v-if="status" class="menu" src="../assets/img/menu.png" @click="openclick" />
        <img v-if="!status" class="menu" src="../assets/img/close.png" @click="closeclick" />
    </div>
    <Content :status="status" />
    <!-- <Footer :status="status" /> -->
    
</template>
<script>
import Content from './Content.vue'
// import Footer from './Footer.vue'
import { ref } from 'vue'

export default {
    name:'HeaderView',
    components:{
        Content,
        // Footer
    },
    setup(){

        const status = ref(true);
        const openclick = (async() => {
            status.value = false;
        })

        const closeclick = (async() => {
            status.value = true;
        })

        return{ status , openclick , closeclick }
    }
}
</script>


<style scoped>
@import '../assets/css/header.css';
</style>   