<template>
  <div class="prizes__main__wrapper">
  <div class="container">
    <div class="prizes__main">
      <div class="left__content">
        <div class="prizes__img__wrapper">
          <img src="@/assets/svgs/trophy.svg" alt="" />
        </div>
      </div>

      <div class="right__content">
        <div class="prizes__text__wrapper">
          <h2>Prizes and <span class="rewards__purple">Rewards</span></h2>
          <p>
            Highlight of the prizes or rewards for winners and for participants.
          </p>
        </div>
        <div class="main__prizes__wrapper">
          <div class="prize__card second__runner">
            <div class="silver__medal__wrapper">
              <img src="@/assets/svgs/silver__medal.svg" alt="" />
            </div>
            <h3 class="position">2nd</h3>
            <p class="text">Runner</p>
            <p class="figure">N300,000</p>
          </div>

          <div class="prize__card first__runner">
            <div class="gold__medal__wrapper">
              <img src="@/assets/svgs/gold__medal.svg" alt="" />
            </div>
            <h3 class="position">1st</h3>
            <p class="text">Runner</p>
            <p class="figure">N400,000</p>
          </div>

          <div class="prize__card third__runner">
            <div class="bronze__medal__wrapper">
              <img src="@/assets/svgs/bronze__medal.svg" alt="" />
            </div>
            <h3 class="position">3rd</h3>
            <p class="text">Runner</p>
            <p class="figure">150,000</p>
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
.prizes__main__wrapper {
  padding-top: 80px;
  padding-bottom: 170px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.18);
}
.prizes__main {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.left__content {
  width: 575px;
}
.right__content {
  width: 575px;
}
.prizes__img__wrapper img {
  width: 100%;
}
.prizes__text__wrapper h2 {
  color: #fff;
  font-family: Clash Display;
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  width: 200px;
}
.rewards__purple {
  color: #d434fe;
  font-family: Clash Display;
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
}
.prizes__text__wrapper {
  padding: 0 100px;
}
.prizes__text__wrapper p {
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 170.9%; /* 27.344px */
  width: 400px;
  margin-top: 15px;
}
.position {
  color: #fff;
  font-family: Montserrat;
  font-size: 26px;
  font-style: normal;
  font-weight: 700;
}
.runner {
  color: #fff;
  font-family: Montserrat;
  font-size: 14px;
  font-style: normal;
  font-weight: 600;
}
.figure {
  color: #d434fe;
  font-family: Montserrat;
  font-size: 22px;
  font-style: normal;
  font-weight: 700;
}
.main__prizes__wrapper {
  display: flex;
  justify-content: space-between;
  margin-top: 300px;
}
.prize__card {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 180px;
}
.second__runner {
  border-radius: 8px;
  border: 1px solid #d434fe;
  background: rgba(212, 52, 254, 0.12);
  height: 200px;
  position: relative;
}

.first__runner {
  position: relative;
  border-radius: 8px;
  border: 1px solid #903aff;
  background: rgba(144, 58, 255, 0.12);
  height: 215px;
}
.third__runner {
  position: relative;
  border-radius: 8px;
  border: 1px solid #d434fe;
  background: rgba(212, 52, 254, 0.12);
  height: 200px;
}
.silver__medal__wrapper {
  position: absolute;
  top: -108px;
}
.second__runner h3,
.third__runner h3 {
  margin-top: 100px;
}

.first__runner h3 {
  margin-top: 110px;
}

.gold__medal__wrapper {
  position: absolute;
  top: -228px;
}
.bronze__medal__wrapper {
  position: absolute;
  top: -108px;
}
@media (max-width: 800px) {
  .prizes__main {
    flex-direction: column;
  }
  .left__content {
    width: 100%;
  }
  .right__content {
    width: 100%;
  }
  .prizes__text__wrapper {
    padding: 0;
  }
  .prizes__text__wrapper h2 {
    font-size: 20px;
    text-align: center;
    margin: 0 auto;
  }
  .rewards__purple {
    font-size: 20px;
  }
  .prizes__text__wrapper p {
    font-size: 12px;
    text-align: center;
    width: 280px;
    margin: 0 auto;
  }
  .position {
    font-size: 12px;
  }
  .runner {
    font-size: 12px;
  }
  .figure {
    font-size: 14px;
  }
  .prize__card {
    width: 120px;
  }
  .silver__medal__wrapper {
    width: 100px;
    top: -50px;
  }
  .silver__medal__wrapper img {
    width: 100%;
  }
  .gold__medal__wrapper {
    width: 160px;
    top: -76px;
  }
  .gold__medal__wrapper img {
    width: 100%;
  }
  .bronze__medal__wrapper {
    width: 100px;
    top: -50px;
  }
  .bronze__medal__wrapper img {
    width: 100%;
  }
  .second__runner {
    height: 170px;
  }
  .first__runner {
    height: 190px;
  }
  .third__runner {
    height: 170px;
  }
  .second__runner h3,
  .third__runner h3 {
    margin-top: 70px;
  }

  .first__runner h3 {
    margin-top: 90px;
  }
}
</style>
