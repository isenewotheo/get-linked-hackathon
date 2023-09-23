<template>
  <header
    :class="{ 'header__no__border-bottom': isContactPage || isRegisterPage }"
  >
    <div class="container">
      <nav class="header__nav">
        <router-link to="/">
          <div class="header__logo">
            <!-- <img src="@/assets/images/logo.svg" alt="" /> -->
            get<span>linked</span>
          </div>
        </router-link>
        <div class="header__links__wrapper">
          <ul class="header__links">
            <li class="header__link">Timeline</li>
            <li class="header__link">Overview</li>
            <li class="header__link">FAQs</li>
            <router-link to="/contact">
              <li class="header__link header__link--contact-link">Contact</li>
            </router-link>
          </ul>
          <router-link to="/register">
            <div
              v-if="isRegisterPage"
              class="header__register-button--outlined-gradient"
            >
              <button>Register</button>
            </div>
            <div v-else class="header__register-button">
              <button>Register</button>
            </div>
          </router-link>
        </div>
        <div class="header__menu-icon__wrapper" @click="openSidenav">
          <img src="@/assets/images/header-menu-icon.svg" alt="" />
        </div>
      </nav>
    </div>
    <Aside class="sidenav__wrapper" ref="sidenav">
      <div class="sidenav__close-icon__wrapper">
        <div class="sidenav__close-icon" @click="closeSidenav()">
          <img src="@/assets/images/circle-gradient.svg" alt="" />
          <img src="@/assets/images/times.svg" alt="" />
        </div>
      </div>
      <nav class="sidenav">
        <div class="sidenav__link"  @click="closeSidenav()">Timeline</div>
        <div class="sidenav__link"  @click="closeSidenav()">Overview</div>
        <div class="sidenav__link"  @click="closeSidenav()">FAQs</div>
        <router-link to="/contact"  @click="closeSidenav()">
          <div class="sidenav__link">Contact</div>
        </router-link>
        <router-link to="/register">
          <div
            v-if="isRegisterPage"
            class="header__register-button--outlined-gradient"
          >
            <button>Register</button>
          </div>
          <div v-else class="header__register-button">
            <button>Register</button>
          </div>
        </router-link>
      </nav>
    </Aside>
  </header>
</template>

<script>
export default {
  data() {
    return {
      showSidenav: false,
    };
  },
  computed: {
    isContactPage() {
      let k = this.$route.path;
      k = k.replace("/", "");
      return k === "contact";
    },
    isRegisterPage() {
      let k = this.$route.path;
      k = k.replace("/", "");
      return k === "register";
    },
  },
  methods: {
    openSidenav() {
      this.$refs.sidenav.classList.add("sidenav__wrapper--slide-in-right");
      this.$refs.sidenav.classList.remove("sidenav__wrapper--slide-out-right");
    },
    closeSidenav() {
      this.$refs.sidenav.classList.add("sidenav__wrapper--slide-out-right");
      this.$refs.sidenav.classList.remove("sidenav__wrapper--slide-in-right");
    },
  },
};
</script>

<style scoped>
header {
  height: var(--header-height);
  z-index: 200;
  position: absolute;
  width: 100%;
  top: 0px;
  left: 0px;
  padding-top: auto;
  border-bottom: 1px solid rgba(255, 255, 255, 0.18);
}
@keyframes slideInRight {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(0);
  }
}
@keyframes slideOutRight {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(100%);
  }
}

.sidenav__wrapper--slide-in-right {
  animation: slideInRight 0.5s ease-in-out forwards;
}
.sidenav__wrapper--slide-out-right {
  animation: slideOutRight 0.5s ease-in-out forwards;
}
.sidenav__wrapper {
  height: 100%;
  width: 100%;
  position: fixed;
  top: 0px;
  left: 0px;
  transform: translateX(100%);
  border-radius: 8px;
  border: 0.5px solid rgba(255, 255, 255, 0.04);
  background: #150e28;
  backdrop-filter: blur(30px);
  padding: 50px;
}
.sidenav__close-icon__wrapper {
  height: 50px;
  display: flex;
  justify-content: flex-end;
  align-items: flex-start;
}
.sidenav__close-icon {
  position: relative;
  width: 23px;
  height: 23px;
}

.sidenav__close-icon img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
.sidenav__close-icon img:last-of-type {
  width: 11px;
  height: 11px !important;
  top: 6px;
  left: 6px;
}
.sidenav {
  display: flex;
  flex-direction: column;
  gap: 16px;
}
.sidenav__link {
  color: #fff;
  font-family: Inter;
  font-size: 18px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  letter-spacing: -1px;
}
.header__no__border-bottom {
  border-bottom: none;
}
.header__logo {
  color: #fff;
  font-family: Clash Display;
  font-size: 36px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
}

.header__logo span {
  color: #d434fe;
}
.header__menu-icon__wrapper {
  display: none;
}
.container {
  height: 100%;
}
.header__nav {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  height: 100%;
  padding-bottom: 30px;
}
.header__links__wrapper {
  display: flex;
  justify-content: space-between;
  gap: 121px;
  align-items: center;
}
.header__links {
  display: flex;
  justify-content: space-between;
  gap: 56px;
}
.header__link {
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  font-weight: 400;
  line-height: normal;
  list-style: none;
  cursor: pointer;
}
.header__link--contact-link {
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  background: linear-gradient(90deg, #903aff 3.08%, #ff26b9 93.85%);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.header__register-button button {
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  border: none;
  outline: none;
  width: 172px;
  height: 53px;
  flex-shrink: 0;
  border-radius: 4px;
  background: linear-gradient(
    270deg,
    #903aff 0%,
    #d434fe 56.42%,
    #ff26b9 99.99%,
    #fe34b9 100%
  );
}
.header__register-button--outlined-gradient button {
  width: 172px;
  height: 53px;
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  background-color: transparent;
  outline: none;
  border: 2px solid #ff29b9;
  border-image-source: linear-gradient(180deg, #9a39ff 0%, #ff29b9 100%);
  border-image-slice: 1;
  border-image-repeat: stretch;
  border-image-width: 2px;
}

@media (max-width: 1100px) {
  .header__links__wrapper {
    gap: 21px;
  }
}
@media (max-width: 900px) {
  .header__logo {
    font-size: 15px;
  }
  .header__links__wrapper {
    display: none;
  }
  .header__menu-icon__wrapper {
    display: block;
  }
  .header__nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100%;
    padding: 0 48px;
  }
}
@media (max-width: 600px) {
  .header__nav {
    padding: 28px;
  }
}
</style>
