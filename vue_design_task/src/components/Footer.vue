<template>
    <div class="navi" v-if="status">
        <div class="home">
            <img class="home-vector" src="../assets/img/icon-24/home.svg">
            <span class="text">ホーム</span>
            <img class="line" src="../assets/img/icon-24/Line_9.svg" />
        </div>
        <div class="barcode">
            <img class="barcode-vector" src="../assets/img/icon-24/barcode.svg" />
            <span class="text">バーコード読取</span>
            <img class="line" src="../assets/img/icon-24/Line_9.svg" />
        </div>
        <div class="box">
            <img class="box-vector" src="../assets/img/icon-24/box.svg" />
            <span class="text">受け取りBOX</span>
            <img class="line" src="../assets/img/icon-24/Line_9.svg" />
        </div>
        <div class="navi-present">
            <img class="navi-present-vector" src="../assets/img/icon-24/present.svg" />
            <span class="text">プレゼント一覧</span>
        </div>
      
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