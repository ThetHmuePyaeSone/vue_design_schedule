<template>
    <div v-if="status">
    <div class="img-preview">
    <img class="title" src="../assets/img/title.png"  />
    <img class="autolayout" src="../assets/img/ポイント.png" />
   </div>
    <div class="content">
    <img class="prearrow" src="../assets/img/arrow/pre.svg" alt="Pre" />
    <img class="nextarrow" src="../assets/img/arrow/next.svg" alt="Next" />
    <p class="pre">前月</p>
    <p class="next">次月</p>
    <p class="year">2022</p>
    <p class="day">09</p>

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
    <img class="" src="../assets/img/line.svg" alt="Line" />
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
    <img class="" src="../assets/img/line.svg" alt="Line" />

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
    <img class="" src="../assets/img/line.svg" alt="Line" />
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
    <img class="" src="../assets/img/line.svg" alt="Line" />

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
<!--     
          <div class="present-panel">
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

            <span class="panel-text">LINEポイント200pt
                プレゼント</span>
          </div>
          <div class="present-panel">
            <img class="panel-img" src="../assets/img/panel/img.png" alt="Img" />

            <div class="img-text">
                <div class="img-frame">
                    <span class="text">LINEポイント</span>
                    <div class="frame-pt">
                      <img class="group" src="../assets/img/panel/Group_110.svg" />
                      <span class="text">100</span>
                    </div>
                </div>
            </div>

            <span class="panel-text">LINEポイント100ptプレゼント</span>
          </div>    

          <div class="present-panel">
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

            <span class="panel-text">LINEポイント200ptプレゼント</span>
          </div>

          <div class="present-panel">
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

            <span class="panel-text">LINEポイント100ptプレゼント</span>
          </div>
          
          <div class="present-panel">
            <img class="panel-img" src="../assets/img/panel/img.png" alt="Img" />

            <div class="img-text">
                <div class="img-frame">
                    <span class="text">LINEポイント</span>
                    <div class="frame-pt">
                      <img class="group" src="../assets/img/panel/Group_110.svg" />
                      <span class="text">100</span>
                    </div>
                </div>
            </div>

            <span class="panel-text">LINEポイント100ptプレゼント</span>
          </div>     -->

    </div>
    <!-- /panel-slide -->
    <div class="present-btn">
            <p class="text">応募可能なプレゼント一覧 </p>
    </div>
</div> 
<!-- /present -->

<div class="contact">

    <div class="contact-title">
        <p class="present-text">CONTACT</p>
        <p class="present-subtitle">お問い合わせ</p>
    </div>
    
    <!-- <div class="contact-title">
        <p class="present">CONTACT</p>
        <p class="text">お問い合わせ</p>
    </div> -->

    <div class="contact-button">
        <div class="button-half-left"><span class="button-half-text left">FAQ</span></div>
        <div class="button-half-right"><span class="button-half-text right">アプリの利用方法</span></div>
    </div>
</div>
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