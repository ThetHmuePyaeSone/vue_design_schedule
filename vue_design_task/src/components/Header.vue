<template>
    <div class="header">
        <img class="vector" src="../assets/img/wilkinson_logo.png" />
        <div>
            <div :class="triggerclass" @click="click">
                <span></span>
                <span></span>
                <span></span>
            </div>
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
        const show=ref(true);
        const triggerclass=ref('menu-trigger')
        const click = (async() => {
            console.log('s',status.value)
            if(status.value === true){
            triggerclass.value='menu-trigger active'
            }else{
            triggerclass.value='menu-trigger'
            }
            status.value = !status.value;
            show.value = !show.value
        })


        return{ status , click, triggerclass, show }
    }
}
</script>


<style scoped>
@import '../assets/css/header.css';
</style>   