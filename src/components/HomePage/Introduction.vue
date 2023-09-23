<template>
  <div class="wrapper">
    <section class="container">
      <div class="introduction__main__wrapper">
        <div class="introduction__main">
          <div class="left__content">
            <div class="tiny__purple__svg__wrapper">
              <img src="@/assets/svgs/tiny__purple.svg" alt="" />
            </div>
            <div class="big__idea__img__wrappper">
              <img src="@/assets/svgs/big__idea.svg" alt="" />
            </div>
            <div class="w__like__svg__wrapper">
              <img src="@/assets/svgs/w__like.svg" alt="" />
            </div>
          </div>

          <div class="right__content">
            <div class="big__idea__text__wrappper">
              <h2>
                Introduction to getlinked
                <span class="tech__hackathon">tech Hackathon 1.0</span>
              </h2>
              <p>
                Our tech hackathon is a melting pot of visionaries, and its
                purpose is as clear as day: to shape the future. Whether you're
                a coding genius, a design maverick, or a concept wizard, you'll
                have the chance to transform your ideas into reality. Solving
                real-world problems, pushing the boundaries of technology, and
                creating solutions that can change the world, that's what we're
                all about!
              </p>
              <div class="star__pu__svg__wrapper">
                <img src="@/assets/svgs/star__pu.svg" alt="" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.wrapper {
  padding-bottom: 60px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.18);
}
.introduction__main__wrapper {
  margin-top: 180px;
  padding: 0 25px;
  margin-bottom: 78px;
}
.introduction__main {
  display: flex;
  justify-content: space-between;
  /* padding: 0 30px; */
}
.left__content {
  width: 575px;
  position: relative;
}
.right__content {
  /* width: 660px;
  min-width: 660px; */
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.big__idea__img__wrappper {
  width: 490px;
  height: 477px;
}
.big__idea__img__wrappper img {
  width: 100%;
}
.big__idea__text__wrappper {
  position: relative;
  margin-top: 65px;
}
.big__idea__text__wrappper h2 {
  color: #fff;
  font-family: Clash Display;
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  width: 422px;
}
.tech__hackathon {
  color: #d434fe;
  font-family: Clash Display;
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
}

.big__idea__text__wrappper p {
  margin-top: 14px;
  line-height: 28px;
  width: 535px;
  height: 165px;
  font-size: 14px;
}
.tiny__purple__svg__wrapper {
  position: absolute;
  left: 0;
  bottom: 258px;
}
.star__pu__svg__wrapper {
  position: absolute;
  top: 0;
  right: 0;
}

.w__like__svg__wrapper {
  position: absolute;
  right: -50px;
  bottom: -15px;
}
@media (max-width: 800px) {
  .introduction__main {
    flex-direction: column;
  }

  .left__content {
    width: 100%;
  }
  .right__content {
    width: 100%;
  }

  .big__idea__img__wrappper img {
    width: 100%;
  }
  .big__idea__text__wrappper h2 {
    font-size: 20px;
    width: 300px;
    text-align: center;
    margin: 20px auto;
  }
  .tech__hackathon {
    font-size: 20px;
  }
  .big__idea__text__wrappper p {
    font-size: 13px;
    text-align: center;
    margin-top: 20px;
    /* width: 300px; */
    margin: 0 auto;
  }
}
@media (max-width: 800px) {
}
</style>
