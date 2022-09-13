<template>
    <div class="navi" v-if="status">
      
        <ul>
            <li><a href=""><img src="../assets/img/icon-24/home.svg">ホーム</a></li>
            <li><a href=""><img src="../assets/img/icon-24/barcode.svg" />バーコード読取</a></li>
            <li><a href=""><img src="../assets/img/icon-24/box.svg" />受け取りBOX</a></li>
            <li><a href=""><img src="../assets/img/icon-24/present.svg" />プレゼント一覧</a></li>
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