<template>
    <div class="navi" v-if="status">
        
        <ul>
            <li><img src="../assets/img/icon-24/home.svg">ホーム</li>
            <li><img src="../assets/img/icon-24/barcode.svg" />バーコード読取</li>
            <li><img src="../assets/img/icon-24/box.svg" />受け取りBOX</li>
            <li><img src="../assets/img/icon-24/present.svg" />プレゼント一覧</li>
        </ul>
      
    </div>
</template>
<script>

export default {
    name:'FooterView',
    props:['status']
}
</script>


<style scoped>
@import '../assets/css/footer.css';
 </style>   