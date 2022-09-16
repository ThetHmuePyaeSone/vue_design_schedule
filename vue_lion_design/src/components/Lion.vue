<template>
  <div class="header-container">
    <div class="container">
      <div class="logo">
        <figure><img src="../assets/img/img-head.png" alt="logo" /></figure>
      </div>
      <span class="header-text">くらしの衛生情報</span>
      <div class="inner-bar pc">
        <ul>
          <li>
            <a class="" href=""
              >衛生のきほん
            <figure class="">
                <img class="swap-on-hover__front-image" src="../assets/img/img-frontdrop.png" />
                <img class="swap-on-hover__back-image" src="../assets/img/img-backdrop.png" />
                </figure>
              </a>
          </li>
          <li>
            <a href=""
              >衛生のはなし
              <figure class="">
                <img class="swap-on-hover__front-image" src="../assets/img/img-frontdrop.png" />
                <img class="swap-on-hover__back-image" src="../assets/img/img-backdrop.png" />
                </figure></a>
          </li>
          <li>
            <a href=""
              >衛生のなやみ
              <figure class="">
                <img class="swap-on-hover__front-image" src="../assets/img/img-frontdrop.png" />
                <img class="swap-on-hover__back-image" src="../assets/img/img-backdrop.png" />
                </figure></a>
          </li>
          <li>
            <a href=""
              >衛生研究情報
              <figure class="">
                <img class="swap-on-hover__front-image" src="../assets/img/img-frontdrop.png" />
                <img class="swap-on-hover__back-image" src="../assets/img/img-backdrop.png" />
              </figure></a>
          </li>
        </ul>
      </div>
      <div class="menu sp">
            <!-- <input id="menu-toggle" type="checkbox" /> -->
            <label class='menu-button-container' for="menu-toggle">
            <div class='menu-button' @click="status = !status"></div>
            </label>
      </div>
    </div>
  </div>
  <!-- /header-container -->
  <div class="banner-container">
    <div class="container">
      <div class="banner">
        <carousel ref="carousel" :item-to-show="1">
          <slide v-for="slide in 3" :key="slide">
            <figure>
              <span
                >見出しカラー#FFFにし、フォントサイズ36px。背景は#000(0.5)、テキストエリア横幅700pxに設定。文字数は64文字</span
              ><img src="../assets/img/img_banner.png" />
            </figure>
             </slide>

          <template #addons>
            <navigation />
           
            <div class="pagination">
              <pagination></pagination>
              <div class="next-slide" @click="next"></div>
            </div>
          </template>
        </carousel>
      </div>
    </div>
  </div>
  <!-- /banner-container -->

  <div class="content-container">
    <div class="container">
      <div class="content-inner">
        <div class="content-title">
          <p class="title">今日から始めるよう！</p>
          <p class="subtitle">衛生のはなし</p>
          <p class="line"></p>
          <p class="info">気になる衛生情報や研究情報など</p>
        </div>
        <div class="content-banner">
          <carousel :breakpoints="breakpoints" ref="carousel" :items-to-show="3">
            <slide v-for="slide in 6" :key="slide">
              <div class="content-slide">
                    <figure>
                      <img src="../assets/img/img-mask1.png" alt="" />
                      <div class="content-text">
                      <button class="content-button">歯磨き</button>
                      <span
                        >感染の入り口＝お口を清潔に保つ～ウイルスが気になる季節に～</span
                      >
                      </div>
                    </figure>

              </div>
            </slide>

            <template #addons>
              <navigation />
              <div class="pagination">
              <pagination></pagination>
              <div class="next-slide" @click="next"></div>
              </div>
              <!-- <div class="next-slide" @click="next"></div> -->
            </template>
          </carousel>
        </div>
      </div>
    </div>
  </div>
  <!-- content-container -->

  <div class="research-container">
    <div class="container">
      <p class="research-title">今日から始めるよう！</p>
      <ul>
        <li
          v-on:click="toggleDetails(media)"
          v-for="media in mediaList"
          :key="media"
          v-show="type === '' || media.type == type"
          v-bind:class="[media.showDetail ? 'less' : 'more', media.type]"
        >
          <div class="research-inner">
            <div class="col-4 date">
              {{ media.date }}
            </div>
            <div class="col-8 description">
              <div>{{ media.description }}</div>
              <div class="show-detail" v-show="media.showDetail">
                <span>{{ media.show }}</span>
                <span>{{ media.time }}</span>
                <span>{{ media.place }}</span>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </div>
  <!-- reserch container -->

  <div class="related-container">
    <div class="container">
      <div class="content-inner">
        <div class="content-title">
          <p class="subtitle">衛生のはなし</p>
          <p class="line"></p>
        </div>
        <div class="related-banner">
          <div class="related-site">
          <figure class="related-img">
            <img src="../assets/img/img-lion.png" alt="" />
          </figure>
            <div class="related-text">
              <span>ライオンハイジーン株式会社</span>
              <figure class="swap-on-hover">
                <img class="swap-on-hover__front-image" src="../assets/img/img-frontexport.png" alt="" />
                <img class="swap-on-hover__back-image" src="../assets/img/img-backexport.png" alt="" />
              </figure>
            </div>
          </div>
          <div class="related-site">
            <figure class="related-img">
            <img src="../assets/img/img-tooth.png" alt="" />
            </figure>
            <div class="related-text">
              <span>日本歯科医師会</span>
              <figure class="swap-on-hover">
                <img class="swap-on-hover__front-image" src="../assets/img/img-frontexport.png" alt="" />
                <img class="swap-on-hover__back-image" src="../assets/img/img-backexport.png" alt="" />
              </figure>
            </div>
          </div>
          <div class="related-site">
            <figure class="related-img">
            <img src="../assets/img/img-stop.png" alt="" />
            </figure>
            <div class="related-text">
              <span>厚生労働省</span>
              <figure class="swap-on-hover">
                <img class="swap-on-hover__front-image" src="../assets/img/img-frontexport.png" alt="" />
                <img class="swap-on-hover__back-image" src="../assets/img/img-backexport.png" alt="" />
              </figure>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="footer-container">
    <div class="container">
      <div class="footer-inner">
        <div class="footer-banner">
          <div class="col-4">
           <figure class="lion-2x"><img src="../assets/img/img-head.png" alt="" /></figure> 
          </div>
          <div class="col-6">
            <ul>
              <li>
                <figure><img src="../assets/img/img_next.png" /></figure>
                <a href="">利用規約</a>
              </li>
              <li>
                <figure><img src="../assets/img/img_next.png" /></figure>
                <a href="">個人情報等の保護について</a>
              </li>

              <li>
                <figure><img src="../assets/img/img_next.png" /></figure>
                <a href="">ソーシャルメディアポリシー</a>
              </li>
            </ul>
          </div>
          <div class="footer-swap">
           <figure class="swap-on-hover">
              <img class="swap-on-hover__front-image" src="../assets/img/img-frontfooter.png" alt="" />
              <img class="swap-on-hover__back-image" src="../assets/img/img-backfooter.png" alt="" />
            </figure>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-bar">
      <span>Copyright© 1996-2022 Lion Corporation. All rights reserved.</span>
    </div>
  </div>
  <!-- footer-container -->
</template>
<script>
/* eslint-disable */
import "../assets/css/reset.css";
import "../assets/css/common.css";
import "../assets/css/common_sp.css"
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";
import { ref } from "vue";
const research = [
  {
    date: "2021年9月8日",
    description: "正しい手洗い、うがい、消毒の方法とその効果について",
    show: "第72回コロイドおよび界面化学討論会",
    type: "book",
    time: "2021/9/15-9/21",
    place: "尾本 百合子",
    showDetail: false,
  },
  {
    date: "2021年9月8日",
    description:
      "家庭内におけるウイルス接触伝播に着目したケア効果可視化の取り組み",
    show: "第72回コロイドおよび界面化学討論会",
    type: "DVD",
    time: "2021/9/15-9/21",
    place: "尾本 百合子",
    showDetail: false,
  },
  {
    date: "2021年9月8日",
    description: "手洗いによる抗菌・抗ウイルス効果の持続性に関する研究",
    show: "第72回コロイドおよび界面化学討論会",
    type: "DVD",
    time: "2021/9/15-9/21",
    place: "尾本 百合子",
    showDetail: false,
  },
  {
    date: "2021年9月8日",
    description:
      "Potential role of oral care practices in preventing SARS-CoV-2 infection in the era of the “new normal”",
    show: "第72回コロイドおよび界面化学討論会",
    type: "book",
    time: "2021/9/15-9/21",
    place: "尾本 百合子",
    showDetail: false,
  },
  {
    date: "2021年9月8日",
    description:
      "新型コロナウイルス(SARS-CoV-2)に対する歯磨剤の不活化効果とそのメカニズム解明",
    show: "第72回コロイドおよび界面化学討論会",
    type: "streaming video",
    time: "2021/9/15-9/21",
    place: "尾本 百合子",
    showDetail: false,
  },
  {
    date: "2021年9月8日",
    description:
      "The inhibitory effects of toothpaste and mouthwash ingredients on the interaction between the SARS-CoV-2 spike protein and ACE2, and the protease activity of TMPRSS2, in vitro",
    show: "第72回コロイドおよび界面化学討論会",
    type: "streaming video",
    time: "2021/9/15-9/21",
    place: "尾本 百合子",
    showDetail: false,
  },
];
export default {
  name: "LionView",
  components: {
    Carousel,
    Slide,
    Navigation,
    Pagination,
  },

  setup() {
    const carousel = ref(null);
    const next = async () => {
      carousel.value.next();
    };
    const mediaList = ref(research);
    const type = ref("");
    const mediaLists = ref([
      {
        title: "Hop on Pop",
        description: "A delightful children's book.",
        type: "book",
        contributor: "Dr. Suess",
        showDetail: false,
      },
      {
        title: "The Joy of Painting",
        description: "Create a world of happy little trees!",
        type: "DVD",
        contributor: "Bob Ross",
        showDetail: false,
      },
      {
        title: "Supernatural: The Complete 12th Season",
        description: "A (literally) neverending roadtrip.",
        type: "DVD",
        contributor: "",
        showDetail: false,
      },
      {
        title: "Planet Earth II",
        description:
          "Hours of beautiful but heart attack-inducing nature footage",
        type: "streaming video",
        contributor: "David Attenborough",
        showDetail: false,
      },
      {
        title: "Titanic",
        description: "The boat sinks.",
        type: "DVD",
        contributor: "James Cameron",
        showDetail: false,
      },
      {
        title: "The Sirens of Titan",
        description:
          "Mankind flung its advance agents ever outward, ever outward... it flung them like stones.",
        type: "book",
        contributor: "Kurt Vonnegut",
        showDetail: false,
      },
      {
        title: "Better Call Saul",
        description: "A slow-burning Breaking Bad prequel.",
        type: "streaming video",
        contributor: "",
        showDetail: false,
      },
    ]);

    const toggleDetails = (media) => {
      media.showDetail = !media.showDetail;
      console.log("media", media.type);
    };

    return {
      next,
      carousel,
      type,
      mediaList,
      toggleDetails,
      settings: {
        itemsToShow: 1,
        snapAlign: "center",
      },
      breakpoints: {
       
        320:{
          itemsToShow: 1,
          snapAlign: "center"
        },
        414: {
          itemsToShow: 1,
          snapAlign: "center",
        },
        1280:{
          itemsToShow: 3,
          snapAlign: "center",
        }
        
      },
    };
  },
};
</script>

