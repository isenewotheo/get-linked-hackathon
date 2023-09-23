<template>
  <div class="partners__main__wrapper">
  <div class="container">
    <div class="partners__main">
      <div class="partners__text__wrapper">
        <h2>Partners and Sponsors</h2>
        <p>
          Getlinked Hackathon 1.0 is honored to have the following major
          companies as its partners and sponsors
        </p>
      </div>
      <div class="partners__content">
        <div class="partners__container">
          <div class="partner__content__top">
            <div class="partners__card">
              <img src="@/assets/svgs/liberty__assured.svg" alt="" />
            </div>
            <div class="vertical__line"></div>
            <div class="partners__card liberty__pay__wrapper">
              <img src="@/assets/svgs/liberty__pay.svg" alt="" />
            </div>
            <div class="vertical__line"></div>

            <div class="partners__card">
              <img src="@/assets/svgs/winwise.svg" alt="" />
            </div>
          </div>
          <div class="lines__wrapper">
            <div class="horizontal__line"></div>
            <div class="horizontal__line"></div>

            <div class="horizontal__line"></div>
          </div>
          <div class="partner__content__bottom">
            <div class="partners__card">
              <img src="@/assets/svgs/whisper.svg" alt="" />
            </div>
            <div class="vertical__line"></div>

            <div class="partners__card">
              <img src="@/assets/svgs/paybox.svg" alt="" />
            </div>
            <div class="vertical__line"></div>

            <div class="partners__card">
              <img src="@/assets/svgs/vuzal.svg" alt="" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.partners__main__wrapper {
  padding-top: 114px;
  padding-bottom: 128px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.18);
}
.partners__text__wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.partners__text__wrapper h2 {
  color: #fff;
  font-family: Clash Display;
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  line-height: 27.5px; /* 85.938% */
}
.partners__text__wrapper p {
  color: #fff;
  text-align: center;
  font-family: Montserrat;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 27.5px; /* 196.429% */
  width: 460px;
  margin-top: 20px;
}
.partners__content {
  border-radius: 5px;
  border: 1px solid #d434fe;
  background: rgba(255, 255, 255, 0.01);
  margin-top: 60px;
}
.partners__container {
  width: 70%;
  /* background-color: red; */
  margin: 150px auto;
}
.partners__card {
  width: 200px;
}
.partners__card img {
  width: 100%;
}

.vertical__line {
  width: 4px;
  height: 112.476px;
  background: #d434fe;
}
.horizontal__line {
  width: 257.298px;
  height: 4px;
  background: #d434fe;
}
.partner__content__top {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.partner__content__bottom {
  display: flex;
  align-items: center;
  justify-content: space-between;
  /* margin-top: 80px; */
}
/* .partners__card img {
  width: 100%;
} */
.lines__wrapper {
  display: flex;
  align-items: center;
  margin: 40px 0;
  gap: 85px;
}
/* .line__wrapper__bottom {
  display: flex;
  align-items: center;
  gap: 40px;
} */

@media (max-width: 800px) {
  .partners__text__wrapper h2 {
    font-size: 20px;
  }
  .partners__text__wrapper p {
    font-size: 12px;
    width: 288px;
    margin: 0 auto;
  }
  .partners__container {
    /* width: 100px; */
    margin: 20px auto;
  }
  .partners__card {
    width: 40px;
    /* height: 80px; */
  }
  .partners__card img {
    width: 100%;
    /* object-fit: contain; */

    /* height: 100%; */
  }
  .partners__content {
    width: 350px;
    margin: 20px auto;
  }
  /* .line__wrapper__bottom {
    gap: 20px;
  } */
  .vertical__line {
    width: 2px;
    height: 29.844px;
  }
  .horizontal__line {
    width: 90px;
    height: 2px;
  }
  .lines__wrapper {
    margin: 10px 0;
    gap: 44px;
  }
  .partners__container {
    width: 100%;
    padding: 0 40px;
  /* width: 60%; */
  }

}
</style>
