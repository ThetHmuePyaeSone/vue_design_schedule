<template>
    <div class="header">
        <img class="vector" src="../assets/img/wilkinson_logo.png" />
        <div class="menu" >
            <input id="menu-toggle" type="checkbox" />
            <label class='menu-button-container' for="menu-toggle">
            <div class='menu-button' @click="status = !status"></div>
            </label>
        </div>
           
        
    </div>
    <Content :status="status" />
    <Footer :status="status" /> 
    
</template>

<script>
import Content from './Content.vue'
import Footer from './Footer.vue'
import { ref } from 'vue'

export default {
    name:'HeaderView',
    components:{
        Content,
        Footer
    },
    setup(){

        const status = ref(true);
        return{ status }
    }
}
</script>


<style scoped>
@import '../assets/css/header.css';
</style>   