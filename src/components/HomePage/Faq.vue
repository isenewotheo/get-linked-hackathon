<template>
  <div class="faq__main__wrapper">
    <div class="container">
      <div class="faq__main">
        <div class="left__content">
          <div class="faq__text__wrapper">
            <h2 class="faq__heading">
              Frequently Ask <span class="question__purple"> Question </span>
            </h2>
            <p class="faq__mini__text">
              We got answers to the questions that you might want to ask about
              getlinked Hackathon 1.0
            </p>
            <div class="questions__wrapper">
              <div class="question">
                <p>Can I work on a project I started before the hackathon?</p>
                <span class="purple__plus">+</span>
              </div>
              <div class="line"></div>
              <div class="question">
                <p>What happens if I need help during the hackathon?</p>
                <span class="purple__plus">+</span>
              </div>
              <div class="line"></div>
              <div class="question">
                <p>What happens if I don't have an idea for a project?</p>
                <span class="purple__plus">+</span>
              </div>
              <div class="line"></div>
              <div class="question">
                <p>Can I join a team or do I have to come with one?</p>
                <span class="purple__plus">+</span>
              </div>
              <div class="line"></div>
              <div class="question">
                <p>What happens after the hackathon ends</p>
                <span class="purple__plus">+</span>
              </div>
              <div class="line"></div>
              <div class="question">
                <p>Can I work on a project I started before the hackathon?</p>
                <span class="purple__plus">+</span>
              </div>
              <div class="line"></div>
            </div>
          </div>
        </div>
        <div class="right__content">
          <div class="faq__img__wrapper">
            <img src="@/assets/svgs/faq.svg" alt="" />
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
.left__content {
  width: 575px;
}
.right__content {
  width: 575px;
}
.faq__main__wrapper {
  margin-top: 80px;
  padding-bottom: 90px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.18);
}
.faq__main {
  display: flex;
  justify-content: space-between;
}
.faq__heading {
  /* color: #fff; */
  /* font-family: Clash Display; */
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  width: 400px;
}
.question__purple {
  color: #d434fe !important;
  /* font-family: Clash Display; */
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  line-height: 0%;
}
.faq__img__wrapper img {
  width: 100%;
}
.faq__mini__text {
  margin-top: 20px;
  line-height: 25px;
  width: 425px;
}
.questions__wrapper {
  margin-top: 40px;
  width: 477px;
}
.line {
  height: 1px;
  width: 100%;
  background: #d434fe;
  margin-top: 15px;
}
.question {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 25px;
}
.purple__plus {
  color: #d434fe;
  font-size: 18px;
}

@media (max-width: 800px) {
  .faq__main {
    flex-direction: column;
  }
  .left__content {
    width: 100%;
  }
  .right__content {
    width: 100%;
  }
  .faq__heading {
    font-size: 20px;
    margin: 0 auto;
    width: 200px;
    text-align: center;
  }
  .question__purple {
    font-size: 20px;
  }
  .faq__mini__text {
    font-size: 12px;
    text-align: center;
    width: 316px;
    margin: 0 auto;
  }
  .questions__wrapper{
    width: 300px;
    margin: 0 auto;

  }
  .question p {
    font-size: 12px;
  }
}
</style>
