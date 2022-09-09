<template>
    <div v-if="status">
        
    <div class="content">
    <div class="pointlog">
       <div><img class="title" src="../assets/img/title.png"  /></div>
       <div class="top">
        <div class="top_yellow">
            <div class="yellow-text">
                <span>あなたの累計ポイント数</span>
                <span class="point">1,000 pt</span>
                <span class="point-line"></span>
            </div>  
            <span>あと0000ptポイントでランクアップ</span>
        </div>
        <div class="top_red">
            <div class="red-text">
                <span>あなたの現在の所持ポイント数</span>
                <span class="point">1,000 pt</span>
            </div>
        </div>

        <div class="show-month">
            <p class="year">2022</p>
            <div class="month">
                <div class="pre-month">
                    <img class="prearrow" src="../assets/img/arrow/pre.svg" alt="Pre" />
                    <span class="pre">前月</span>
                </div>
                <div>
                    <span class="day">09</span>
                </div>
                <div class="next-month">
                    <span class="next">次月</span>
                    <img class="nextarrow" src="../assets/img/arrow/next.svg" alt="Next" />
                </div>
            </div>
        </div>
              
<div class="list">
    <div class="item">
        <img class="thumbnail-80" src="../assets/img/rect_wilkinson.png" />
        <div class="frame-292">
            <span class="frame-date">2022/9/2</span>
            <span class="frame-text">ウィルキンソン炭酸水</span>
            <span class="frame-text">500ml</span>
        </div>
        <div class="pt">
            <div class="pt-text">
                <span>+</span>
                <span>1000</span>
                <span>pt</span>
            </div>
        </div>
    </div>
    
    <div class="item">
        <img class="thumbnail-80" src="../assets/img/rect_line.png" />
        <div class="frame-292">
            <span class="frame-date">2022/9/2</span>
            <span class="frame-text">LINE POINT</span>
            <span class="frame-text">XXpt</span>
        </div>
        <div class="pt">
            <div class="pt-minus">
                <span>-</span>
                <span>20</span>
                <span>pt</span>
            </div>
        </div>
    </div>
    

    <div class="item">
        <img class="thumbnail-80" src="../assets/img/rect_wilkinson.png" />
        <div class="frame-292">
            <span class="frame-date">2022/9/2</span>
            <span class="frame-text">ウィルキンソン炭酸水</span>
            <span class="frame-text">500ml</span>
        </div>
        <div class="pt">
            <div class="pt-text">
                <span>+</span>
                <span>1000</span>
                <span>pt</span>
            </div>
        </div>
    </div>
    
    <div class="item">
        <img class="thumbnail-80" src="../assets/img/rect_line.png" />
        <div class="frame-292">
            <span class="frame-date">2022/9/2</span>
            <span class="frame-text">LINE POINT</span>
            <span class="frame-text">XXpt</span>
        </div>
        <div class="pt">
            <div class="pt-minus">
                <span>-</span>
                <span>20</span>
                <span>pt</span>
            </div>
        </div>
    </div>

</div> 
<!-- /list --> 

<div class="present-content">
    <div class="present-title">
        <p class="present-text">PRESENT</p>
        <p class="present-subtitle">貯めたポイントで応募する！</p>
    </div>

  <div class="present-slide">

        <carousel :settings="settings" :breakpoints="breakpoints">
		<slide v-for="slide in 5" :key="slide">
            <div class="present-panel carousel__item">
            <img class="panel-img" src="../assets/img/panel/img.png" alt="Img" />
            
            <div class="img-text">
                <div class="img-frame">
                    <span class="text">LINEポイント</span>
                    <div class="frame-pt">
                      <img class="group" src="../assets/img/panel/Group_110.svg" />
                      <span class="text">200</span>
                    </div>
                </div>
            </div>

            <div class="panel-text">
                <span>LINEポイント200pt</span>
                <span>プレゼント</span>
            </div>
          </div>

		</slide>
		<template #addons>
			<navigation />
		</template>
	</carousel>
    </div>
    
    <div class="present-btn">
            <p class="text">応募可能なプレゼント一覧 </p>
    </div> 
</div> 
<!-- /present -->
       </div>
 
    </div>
<!-- /point log -->


<!-- 
<div class="contact">

    <div class="contact-title">
        <p class="present-text">CONTACT</p>
        <p class="present-subtitle">お問い合わせ</p>
    </div>
    
    <div class="contact-button">
        <div class="button-half-left"><span class="button-half-text left">FAQ</span></div>
        <div class="button-half-right"><span class="button-half-text right">アプリの利用方法</span></div>
    </div>
</div> -->
<!-- /contact -->
</div>
</div>
<!-- /all content -->

<div v-if="!status">
    <div class="menuframe">
        <img class="" src="../assets/img/line.svg" alt="Line" />
        <div class="menu-home">
            <img class="" src="../assets/img/icon-24/home.svg">
            <span class="text">ホーム</span>
        </div>
        <img class="" src="../assets/img/line.svg" alt="Line" />
        <div class="menu-home">
            <img class="" src="../assets/img/icon-24/menu_barcode.svg">
            <span class="text">バーコード読み取り</span>
        </div>  
        <img class="" src="../assets/img/line.svg" alt="Line" />
        <div class="menu-home">
            <img class="" src="../assets/img/icon-24/point.svg">
            <span class="text">ポイント履歴</span>
        </div>
        <img class="" src="../assets/img/line.svg" alt="Line" />
        <div class="menu-home">
            <img class="" src="../assets/img/icon-24/present.svg">
            <span class="text">プレゼント一覧</span>
        </div>  
        <img class="" src="../assets/img/line.svg" alt="Line" />
        <div class="menu-home">
            <img class="" src="../assets/img/icon-24/box.svg">
            <span class="text">受け取りBOX</span>
        </div>
        <img class="" src="../assets/img/line.svg" alt="Line" />    
        
        <div class="menu-button">
        <div class="button-half-left"><span class="button-half-text left">FAQ</span></div>
        <div class="button-half-right"><span class="button-half-text right">アプリの利用方法</span></div>
    </div>
    
    </div>
    
</div>
<!-- /menu content -->

</template>
<script>
 import { Carousel, Slide, Navigation } from 'vue3-carousel';
export default {
name:'ContentView',
props:['status'],
components: {
    Carousel,
    Slide,
    Navigation,
},
setup() {
    
    return {
        //carousel settings
        settings: {
            itemsToShow: 2.5,
            snapAlign: "center",
            infinite: true,
            wrapAround: true,
            transition: 300,
            // autoplay: true,
            // autoplaySpeed: 1000
        },
        // breakpoints are mobile first
        // any settings not specified will fallback to the carousel settings
        breakpoints: {
            // 700px and up
            700: {
                itemsToShow: 2.5,
                snapAlign: "center",
            },
            
        }
    };
}

}
</script>

<style scoped>
@import '../assets/css/content.css';
 </style>   