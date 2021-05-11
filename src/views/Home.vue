<template>
  <div>
    <Swiper :swiperOption="swiperOption">
      <template #0>
        <div class="animal">
          <div class="animal-left">
            <div class="animal-left-title">
              <h4>流浪動物之家</h4>
              <p>
                這幾年逐漸流行飼養家庭寵物，隨著養育率提高，棄養率也隨之升高，那些逞一時的新鮮感卻讓毛小孩們有一輩子的陰影，提倡領養代替購買。珍惜身邊的毛小孩。
              </p>
              <div class="animal-left-title-go">
                <a
                  href="https://shiauweitsung.github.io/StrayAnimal/#/"
                  target="_blank"
                  >Go</a
                >
              </div>
            </div>
            <div class="animal-left-info">
              <div class="animal-left-info-descript">
                <p>我很乖巧 很聽話 也很聰明 <br />快來領養我 ~</p>
                <div></div>
              </div>
            </div>
          </div>
          <div class="animal-right"></div>
        </div>
      </template>
      <template #1>
        <div class="razer">
          <div class="razer-left">
            <div class="razer-left-img">
              <img src="~@/assets/images/razer.jpg" alt="" />
            </div>
          </div>
          <div class="razer-right">
            <div class="razer-right-title">電競商品</div>
            <div class="razer-right-info">
              <p>擁有全部雷蛇經典商品代理、歡迎前往選購</p>
              <a href="">前往</a>
            </div>
          </div>
          <div class="razer-bg"></div>
          <div class="razer-bg2"></div>
        </div>
      </template>
      <template #2>
        <div class="vr">
          <div class="vr-bg"></div>
          <div class="vr-info">
            <h4>VR 虛擬實境</h4>
            全新技術．全新體驗 讓你意想不到的新玩法。<br />
            還在體驗一般的電腦遊戲嗎? 現在正夯的VR虛擬實境、VR電競，趕快來體驗。
            <br />
            高科技VR頭顯、智能VR手把感應器、360度廣角定位、4K超清畫質、60fps，極致尊榮體驗。
            <br />
            <a
              href="https://shiauweitsung.github.io/VueVR/#/"
              class="vr-info-link"
              target="_blank"
              >立即前往</a
            >
          </div>
          <div class="vr-list">
            <div>
              <img src="~@/assets/images/vr-head.png" alt="" />
            </div>
            <div>
              <img src="~@/assets/images/vr-hand.png" alt="" />
            </div>
            <div>
              <img src="~@/assets/images/vr-control.png" alt="" />
            </div>
          </div>
        </div>
      </template>
    </Swiper>
  </div>
</template>

<script>
import Swiper from '../components/SwiperCarousel.vue';

export default {
  components: {
    Swiper,
  },
  data() {
    return {
      swiperOption: {
        loop: true,
        class: {
          wrap: 'index-swiper-wrap',
        },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },
        pagination: {
          el: '.swiper-pagination',
          clickable: true,
        },
      },
    };
  },
};
</script>
<style lang="scss" >
.index-swiper-wrap {
  height: calc(100vh - 70px) !important;
  @media (max-width: 768px) {
    height: calc(100vh - 56px) !important;
  }
}
</style>
