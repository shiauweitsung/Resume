<template>
  <div class="header">
    <div class="header-wrap">
      <div class="header-wrap-logo">shiauWeiTsung</div>
      <div
        class="header-wrap-list"
        :class="{ 'active-list': menuShow }"
        @click="closeMenu"
      >
        <ul :class="{ 'active-ul': menuShow }">
          <li><router-link to="/aboutme">關於我</router-link></li>
          <li><router-link to="">作品區</router-link></li>
          <li><router-link to="">聯絡我</router-link></li>
        </ul>
      </div>
      <button
        class="header-wrap-list-mob"
        @click="menuShow = !menuShow"
        :class="{ 'active-btn': menuShow }"
      >
        <span></span>
        <span></span>
        <span></span>
      </button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      menuShow: false,
    };
  },
  methods: {
    closeMenu(e) {
      if (e.target.firstChild.classList.contains('active-ul')) {
        this.menuShow = false;
      }
    },
  },
};
</script>
<style lang="scss">
.header {
  &-wrap {
    max-width: 1440px;
    width: 90%;
    margin: auto;
    display: grid;
    color: #222222;
    grid-template-columns: 300px 1fr;
    padding: 10px;
    @media (max-width: 768px) {
      display: flex;
      justify-content: center;
      position: relative;
    }
    &-logo {
      margin-top: 20px;
    }
    &-list {
      @media (max-width: 768px) {
        position: fixed;
        left: 0px;
        top: 0px;
        height: 100vh;
        width: 0%;
        z-index: 2;
      }
      & > ul {
        display: flex;
        margin-top: 20px;
        @media (max-width: 768px) {
          visibility: visible;
          position: absolute;
          flex-direction: column;
          align-items: center;
          margin-top: 0px;
          left: 0px;
          top: 0px;
          padding: 0px;
          background-color: #efefef;
          width: 150px;
          height: 100vh;
          transition: ease-in-out 0.4s;
          transform: translateX(-150px);
          z-index: 999;
        }

        & > li {
          width: 100px;
          list-style: none;
          @media (max-width: 768px) {
            margin-top: 15px;
            padding: 0px 20px;
            width: auto;
          }
          & > a {
            color: #222222;
            position: relative;
            &::after {
              content: '';
              position: absolute;
              bottom: -5px;
              left: -5px;
              width: 0;
              height: 2px;
              background-color: #222222;
              transition: ease-in-out 0.4s;
            }
          }
          &:hover {
            & > a::after {
              width: calc(100% + 5px);
            }
          }
        }
      }
      &-mob {
        display: none;
        flex-direction: column;
        align-items: center;
        width: 36px;
        height: 36px;
        @media (max-width: 768px) {
          display: flex;
          position: absolute;
          right: 0px;
          margin-top: 15px;
          z-index: 99999999;
        }
        & > span {
          display: block;
          width: 80%;
          height: 1px;
          margin-top: 6px;
          background-color: #222222;
          transition: ease-in-out 0.4s;
          position: relative;
        }
      }
    }
    .active-list {
      @media (max-width: 768px) {
        width: 100%;
        background-color: rgba(71, 71, 71, 0.5);
      }
      & > ul {
        visibility: visible;
        transform: translateX(0px);
      }
    }
    .active-btn {
      & > span {
        background-color: white;
      }
      & > span:nth-of-type(1) {
        top: 6px;
        transform: rotate(-45deg);
      }
      & > span:nth-of-type(2) {
        opacity: 0;
      }
      & > span:nth-of-type(3) {
        top: -8px;
        transform: rotate(45deg);
      }
    }
  }
}
</style>
