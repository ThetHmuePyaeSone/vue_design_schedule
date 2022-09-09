<template>
    
  
    <img class="title" src="../assets/img/title.png"  />
    <img class="autolayout" src="../assets/img/ポイント.png" />

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
        <span class="present-text">PRESENT</span>
        <span class="present-subtitle">貯めたポイントで応募する！</span>
    </div>
    <div class="present-slide">
        <div class="slide-list">
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

        </div>
    </div>
    <!-- /panel-slide -->
    <div class="present-btn">
            <span class="text">応募可能なプレゼント一覧 </span>
    </div>
</div> 
<!-- /present -->

<div class="contact">
    <div class="contact-title">
        <span class="present">CONTACT</span>
        <span class="text">お問い合わせ</span>
    </div>
    <div class="contact-button">
        <div class="button-half-left"><span class="button-half-text left">FAQ</span></div>
        <div class="button-half-right"><span class="button-half-text right">アプリの利用方法</span></div>
    </div>
</div>
<!-- /contact -->



</div>

</template>
<script>
import { Carousel, Slide, Navigation } from 'vue3-carousel';
export default {
name:'ContentView',
components: {
Carousel,
Slide,
Navigation,
},
setup() {
    return {
        // carousel settings
        settings: {
            itemsToShow: 2.5,
            snapAlign: "center"
        },
        // breakpoints are mobile first
        // any settings not specified will fallback to the carousel settings
        breakpoints: {
            // 700px and up
            700: {
                itemsToShow: 2.5,
                snapAlign: "center"
            },
            
        }
    };
}

}
</script>

<style scoped>
@import '../assets/css/content.css';
 </style>   