<template>
  <div class="criteria__main__wrapper">
    <div class="container">
      <div class="criteria__main">
        <div class="left__content">
          <div class="ellipse__one__wrapper">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="134"
              height="134"
              viewBox="0 0 134 134"
              fill="none"
            >
              <circle cx="67" cy="67" r="67" fill="url(#paint0_linear_70_6)" />
              <defs>
                <linearGradient
                  id="paint0_linear_70_6"
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
          <div class="criteria__img__wrapper">
            <img src="@/assets/svgs/criteria.svg" alt="" />
          </div>
        </div>
        <div class="right__content">
          <div class="criteria__text__wrapper">
            <h2>
              Judging Criteria
              <span class="criteria__purple"> Key attributes</span>
            </h2>
            <div class="criteria__list__wrapper">
              <div class="criteria__list">
                <p>
                  <span class="judge__purple">Innovation and Creativity : </span
                  >Evaluate the uniqueness and creativity of the solution.
                  Consider whether it addresses a real-world problem in a novel
                  way or introduces innovative features.
                </p>
              </div>
              <div style="margin-top: 20px" class="criteria__list">
                <p>
                  <span class="judge__purple">Functionality : </span>Assess how
                  well the solution works. Does it perform its intended
                  functions effectively and without major issues? Judges would
                  consider the completeness and robustness of the solution.
                </p>
              </div>
              <div style="margin-top: 20px" class="criteria__list">
                <p>
                  <span class="judge__purple">Impact and Relevance : </span
                  >Determine the potential impact of the solution in the real
                  world. Does it address a significant problem, and is it
                  relevant to the target audience? Judges would assess the
                  potential social, economic, or environmental benefits.
                </p>
              </div>
              <div style="margin-top: 20px" class="criteria__list">
                <p>
                  <span class="judge__purple">Technical Complexity : </span
                  >Evaluate the technical sophistication of the solution. Judges
                  would consider the complexity of the code, the use of advanced
                  technologies or algorithms, and the scalability of the
                  solution.
                </p>
              </div>
              <div style="margin-top: 20px" class="criteria__list">
                <p>
                  <span class="judge__purple"
                    >Adherence to Hackathon Rules : </span
                  >Judges will Ensure that the team adhered to the rules and
                  guidelines of the hackathon, including deadlines, use of
                  specific technologies or APIs, and any other
                  competition-specific requirements.
                </p>
              </div>
            </div>
            <div class="btn__read__more__wrapper">
              <button class="btn btn__read">Read More</button>
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
.criteria__main__wrapper {
  padding-top: 60px;
  padding-bottom: 90px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.18);
}
.criteria__main {
  display: flex;
  justify-content: space-between;
  align-items: center;
  /* margin-top: 20px; */
}
.criteria__text__wrapper h2 {
  color: #fff;
  font-family: Clash Display;
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  width: 280px;
}
.criteria__img__wrapper {
  margin-top: 45px;
  position: relative;
}

.criteria__img__wrapper img {
  width: 100%;
}
.criteria__purple {
  color: #d434fe;
  font-family: Clash Display;
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
}
.left__content {
  width: 575px;
  position: relative;
}
.right__content {
  width: 575px;
}
.criteria__list__wrapper {
  margin-top: 20px;
}
.btn__read {
  margin-top: 40px;
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
}
.criteria__list p {
  color: #fff;
  font-family: Montserrat;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 173.5%;
}
.judge__purple {
  color: #ff26b9;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 700;
  line-height: 173.5%; /* 27.76px */
}
.ellipse__one__wrapper {
  position: absolute;
  left: 72px;
  top: -10px;
}
@media (max-width: 800px) {
  .criteria__main {
    flex-direction: column;
  }
  .left__content {
    width: 100%;
  }
  .right__content {
    width: 100%;
  }
  .criteria__text__wrapper h2 {
    font-size: 20px;
    text-align: center;
    width: 192px;
    margin: 0 auto;
  }
  .criteria__purple {
    font-size: 20px;
  }
  .criteria__list p {
    font-size: 13px;
    text-align: center;
    width: 350px;
    margin: 0 auto;
  }
  .btn__read__more__wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
}
</style>
