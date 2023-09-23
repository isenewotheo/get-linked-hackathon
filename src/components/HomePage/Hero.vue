<template>
  <div class="hero__main__wrapper">
    <div class="container" style="height: 100%">
      <div class="hero__main">
        <div class="ignite__wrapper">
          <h1>Igniting a Revolution in HR Innovation</h1>
          <div class="svg__wrapper__des">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="140"
              height="17"
              viewBox="0 0 255 17"
              fill="none"
            >
              <path
                d="M1 14.043C43.3333 5.7097 154.4 -5.95697 254 14.043"
                stroke="#FF26B9"
                stroke-width="5"
              />
            </svg>
          </div>
          <div class="svg__wrapper__mob">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="140"
              height="17"
              viewBox="0 0 255 17"
              fill="none"
            >
              <path
                d="M1 14.043C43.3333 5.7097 154.4 -5.95697 254 14.043"
                stroke="#FF26B9"
                stroke-width="5"
              />
            </svg>
          </div>
        </div>

        <div class="hero__content">
          <div class="left__content">
            <div class="star__svg__wrapper">
              <img src="@/assets/svgs/star.svg" alt="" />
            </div>
            <div class="left__text__wrapper">
              <div class="bulb__svg__wrapper">
                <img src="@/assets/svgs/bulb.svg" alt="" />
              </div>

              <h2>
                getlinked Tech Hackathon
                <span class="one__point__zero">1.0</span>
                <img src="@/assets/svgs/chain.svg" />
                <img src="@/assets/svgs/spike.svg" />
              </h2>
              <p class="sub__text">
                Participate in getlinked tech Hackathon 2023 stand <br />
                a chance to win a Big prize
              </p>
            </div>

            <div class="btn__register__wrapper">
              <button class="btn btn__register">Register</button>
            </div>
            <div class="countdown__wrapper">
              <div class="countdown">00<span>H</span></div>
              <div class="countdown">00<span>M</span></div>
              <div class="countdown">00<span>S</span></div>
            </div>
            <div class="star__grey__svg__wrapper">
              <img src="@/assets/svgs/star__grey.svg" alt="" />
            </div>
          </div>

          <div class="right__content">
            <div class="star__right__svg__wrapper">
              <img src="@/assets/svgs/star__grey.svg" alt="" />
            </div>
            <div class="hero__img__wrapper">
              <img src="@/assets/svgs/hero__img.svg" alt="" />
            </div>
            <div class="sub__hero_img__wrapper">
              <img src="@/assets/svgs/sub__hero__img.svg" alt="" />
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
.hero__main__wrapper {
  margin-top: var(--header-height);
  height: 737px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.18);
}
.hero__main {
  margin-top: 20px;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: stretch;
  justify-content: space-between;
  padding-top: 32px;
}
.ignite__wrapper {
  display: flex;
  justify-content: flex-end;
  position: relative;
}
.ignite__wrapper h1 {
  color: #fff;
  font-family: Montserrat;
  font-size: 36px;
  font-style: italic;
  font-weight: 700;
  line-height: normal;
}
.hero__content {
  display: flex;
  justify-content: space-between;
  margin-top: 25px;
  align-items: center;
}
.left__content {
  width: 730px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  position: relative;
  /* padding-bottom: 50px; */
}
.right__content {
  width: 575px;
  position: relative;
}
.left__content h2 {
  color: #fff;
  font-family: Clash Display;
  font-size: 80px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  margin-bottom: 8px;
}
.left__content h2 img {
  display: inline;
}
.left__content h2 img:first-of-type {
  display: inline;
  margin-bottom: -20px;
}
.one__point__zero {
  color: #d434fe;
}
.hero__img__wrapper {
  width: 100%;
  /* background-color: red; */
}
.hero__img__wrapper img {
  width: 100%;
  margin-bottom: -4px;
}
.sub__text {
  color: #fff;
  font-family: Montserrat;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 33.2px;
  margin-bottom: 8px;
}
.btn__register__wrapper {
  margin-top: 20px;
}
.btn__register {
  border-radius: 4px;
  background: linear-gradient(
    270deg,
    #903aff 0%,
    #d434fe 56.42%,
    #ff26b9 99.99%,
    #fe34b9 100%
  );
  width: 155px;
  color: #fff;
  padding: 18px 0;
  font-family: Montserrat;
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}
.countdown__wrapper {
  margin-top: 40px;
  display: flex;
  gap: 20px;
}
.countdown {
  color: #fff;
  font-family: Unica One;
  font-size: 64px;
  font-style: normal;
  font-weight: 400;
  line-height: 133%;
  margin-bottom: 50px;
}
.countdown span {
  font-size: 14px;
  font-family: Montserrat;
}
.svg__wrapper__des {
  position: absolute;
  bottom: -23px;
}
.svg__wrapper__mob {
  display: none;
}
.star__svg__wrapper {
  position: absolute;
  top: -16px;
  left: 41px;
}
.left__text__wrapper {
  position: relative;
}
.bulb__svg__wrapper {
  position: absolute;
  right: 126px;
  top: -62px;
}
.chain__svg__wrapper {
  position: absolute;
  right: 45px;
  bottom: 56px;
}
.spike__svg__wrapper {
  position: absolute;
  right: -12px;
  bottom: 69px;
}
.star__grey__svg__wrapper {
  position: absolute;
  bottom: 145px;
  right: 206px;
}
.sub__hero_img__wrapper {
  position: absolute;
  bottom: 0;
}
.star__right__svg__wrapper {
  position: absolute;
}
@media (max-width: 800px) {
  .svg__wrapper__des {
    display: none;
  }
  .hero__main__wrapper {
    margin-top: 20px;
  }
  .ignite__wrapper {
    /* background-color: red; */
    justify-content: center;
    margin-top: 100px;
  }
  .ignite__wrapper h1 {
    font-size: 18px;
  }
  .svg__wrapper__mob {
    display: block;
    position: absolute;
    right: 19px;
    top: 22px;
  }
  .hero__content {
    flex-direction: column;
    margin-top: 40px;
  }
  .left__content {
    width: 100%;
    margin-top: 40px;
  }
  .right__content {
    width: 100%;
  }
  .left__content h2 {
    font-size: 32px;
    text-align: center;
  }
  .one__point__zero {
    font-size: 32px;
  }
  .sub__text {
    width: 350px;
    font-size: 13px;
    text-align: center;
    width: 272px;
    margin: 15px auto;
  }
  .btn__register__wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .countdown {
    text-align: center;
  }
}
</style>
