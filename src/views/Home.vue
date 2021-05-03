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
              <div>
                <a
                  href="https://shiauweitsung.github.io/StrayAnimal/#/"
                  target="_blank"
                  >前往</a
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
            <div class="razer-left-img"></div>
          </div>
          <div class="razer-right">
            <div class="razer-right-title">ShiauRazer</div>
            <div class="razer-right-info">
              <p>123456</p>
              <a href="">前往</a>
            </div>
          </div>
        </div>
      </template>
      <template #2>
        <div class="vr">
          <div class="vr-left">
            <div class="vr-left-title">
              <h4>vr title</h4>
            </div>
            <div class="vr-left-cont">
              <div class="vr-left-cont-info">description</div>
              <div class="vr-left-cont-btn">
                <button>click</button>
              </div>
            </div>
          </div>
          <div class="vr-right">
            <p>背景圖 or img</p>
            <p>浮動標題</p>
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
}
</style>
