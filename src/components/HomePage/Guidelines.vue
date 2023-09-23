<template>
  <div class="guidelines__main__wrapper ">
    <div class="container">
      <div class="guidelines__main">
        <div class="left__content">
          <div class="rules__text__wrapper">
            <h2>Rules and <span class="purple__rules">Guidelines</span></h2>
            <p>
              Our tech hackathon is a melting pot of visionaries, and its purpose
              is as clear as day: to shape the future. Whether you're a coding
              genius, a design maverick, or a concept wizard, you'll have the
              chance to transform your ideas into reality. Solving real-world
              problems, pushing the boundaries of technology, and creating
              solutions that can change the world, that's what we're all about!
            </p>
          </div>
        </div>
        <div class="right__content">
          <div class="ellipse__one__wrapper">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="134"
              height="134"
              viewBox="0 0 134 134"
              fill="none"
            >
              <circle cx="67" cy="67" r="67" fill="url(#paint0_linear_65_65)" />
              <defs>
                <linearGradient
                  id="paint0_linear_65_65"
                  x1="134"
                  y1="67"
                  x2="3.69183"
                  y2="67"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#8F01FE" />
                  <stop offset="1" stop-color="#FF2674" />
                </linearGradient>
              </defs>
            </svg>
          </div>
          <div class="rules__img__wrapper">
            <img src="@/assets/svgs/rules.svg" alt="" />
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
.guidelines__main__wrapper {
  padding-bottom: 20px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.18);
}
.guidelines__main {
  display: flex;
  justify-content: space-between;
}
.left__content {
  width: 575px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
/* .rules__text__wrapper {
} */
.right__content {
  width: 575px;
  position: relative;
}
.rules__text__wrapper h2 {
  color: #fff;
  font-family: Clash Display;
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  width: 170px;
}
.purple__rules {
  color: #d434fe;
  font-family: Clash Display;
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  /* line-height: 0%; */
}

.rules__text__wrapper p {
  color: #fff;
  font-family: Montserrat;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 27.5px; /* 196.429% */
  margin-top: 20px;
}
.ellipse__one__wrapper {
  position: absolute;
  right: 47px;
  top: 110px;
}
.rules__img__wrapper img {
  position: relative;
}

@media (max-width: 800px) {
  .guidelines__main {
    flex-direction: column-reverse;
  }
  .right__content {
    width: 100%;
  }
  .left__content {
    width: 100%;
  }
  .rules__text__wrapper h2 {
    font-size: 20px;
    text-align: center;
    margin: 0 auto;
  }
  .purple__rules {
    font-size: 20px;

  }

 /* .rules__img__wrapper {
      width: 400px;
      margin: 0 auto;


  } */
  .rules__img__wrapper img {
    width: 100%;
  }
  .rules__text__wrapper p {
    font-size: 13px;
    width: 350px;
    text-align: center;
    margin: 20px auto;
  }

}
</style>
