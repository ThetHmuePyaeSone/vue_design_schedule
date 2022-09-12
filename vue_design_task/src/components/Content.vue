<template>
  <div class="container" v-if="status">
    <div class="inner">
      <div class="top-yellow">
        <div class="yellow-text">
          <span>あなたの累計ポイント数</span>
          <span class="point">1,000 pt</span>
          <p class="border-line">
            あと<span class="num-pt">0000pt</span>ポイントでランクアップ
          </p>
        </div>
      </div>
      <div class="top-red">
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
            <span>前月</span>
          </div>
          <div>
            <span class="day">09</span>
          </div>
          <div class="next-month">
            <span class="next">次月</span>
            <img class="" src="../assets/img/arrow/next.svg" alt="Next" />
          </div>
        </div>
      </div>
      <!-- /show-month -->

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
          <carousel
            :settings="settings"
            :breakpoints="breakpoints"
            :items-to-show="2.5"
          >
            <slide v-for="slide in 5" :key="slide">
              <div class="present-panel carousel__item">
                <img
                  class="panel-img"
                  src="../assets/img/panel/img.png"
                  alt="Img"
                />

                <div class="img-text">
                  <div class="img-frame">
                    <span class="text">LINEポイント</span>
                    <div class="frame-pt">
                      <img
                        class="group"
                        src="../assets/img/panel/Group_110.svg"
                      />
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
          <p class="text">応募可能なプレゼント一覧</p>
        </div>
      </div>
      <!-- /present -->

      <div>
        <div class="contact-title">
          <p class="present-text">CONTACT</p>
          <p class="present-subtitle">お問い合わせ</p>
        </div>

        <div class="contact-button">
          <div class="button-half-right">
            <span class="font-barlow">FAQ</span>
          </div>
          <div class="button-half-right">
            <span>アプリの利用方法</span>
          </div>
        </div>
      </div>
      <!-- /contact -->
    </div>
    <!-- /point -->
  </div>
  <!-- /container log -->

  <div v-if="!status" class="menuframe">
    <transition name="slide-fade">
      <div class="menu-inner">
        <ul>
          <li><img class="" src="../assets/img/icon-24/home.svg" />ホーム</li>
          <li>
            <img
              class=""
              src="../assets/img/icon-24/menu_barcode.svg"
            />バーコード読み取り
          </li>
          <li>
            <img class="" src="../assets/img/icon-24/point.svg" />ポイント履歴
          </li>
          <li>
            <img
              class=""
              src="../assets/img/icon-24/present.svg"
            />プレゼント一覧
          </li>
          <li>
            <img class="" src="../assets/img/icon-24/box.svg" />受け取りBOX
          </li>
        </ul>

        <div class="contact-button">
          <div class="button-half-right">
            <span class="font-barlow">FAQ</span>
          </div>
          <div class="button-half-right">
            <span>アプリの利用方法</span>
          </div>
        </div>
      </div>
    </transition>
  </div>
  <!-- /menu content -->
</template>
<script>
/* eslint-disable */
import { Carousel, Slide, Navigation } from "vue3-carousel";
export default {
  name: "ContentView",
  props: ["status"],

  components: {
    Carousel,
    Slide,
    Navigation,
  },
  setup() {
    return {
      settings: {
        infinite: true,
        wrapAround: true,
        transition: 300,
      },
    };
  },
};
</script>

<style scoped>
@import "../assets/css/main.css";
</style>   