<template>
  <div class="reg-suc__modal__scrim" @click.self="back()">
    <div class="reg-suc__modal">
      <div class="reg-suc__modal__image">
        <img src="@/assets/images/reg-suc-congratulations.svg" alt="" />
      </div>
      <div class="reg-suc__modal__title">
        Congratulations <br />
        you have successfully Registered!
      </div>
      <div class="reg-suc__modal__subtitle">
        Yes, it was easy and you did it! <br />
        check your mail box for next step
        <img
          src="@/assets/images/wink-emoji-woman.svg"
          alt="wink emoji woman"
          style="margin-bottom: -3px"
        />
      </div>
      <button class="reg-suc__modal__back-button" @click="back()">Back</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    back() {
      this.$emit("back");
    },
  },
};
</script>

<style scoped>
.reg-suc__modal__scrim {
  background: rgba(21, 14, 40, 0.93);
  width: 100%;
  height: 100%;
  top: 0px;
  left: 0px;
  position: fixed;
  z-index: 200;
  display: grid;
  place-items: center;

  background-position: 70% 148px;
  background-image: url(@/assets/images/register-form-purple-star.svg);
  /* background-blend-mode: hard-light;s */
  background-repeat: no-repeat;
}

.reg-suc__modal {
  padding: 34px 71px 73px 54px;
  /* padding-top: ; */
  width: 699px;
  height: 664px;
  flex-shrink: 0;
  border-radius: 5px;
  border: 1px solid #d434fe;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  transition: all 90ms;

  /* background-color: green; */

  background-position: 88px 241px, 631px 619px;
  background-image: url(@/assets/images/register-form-star-lightgrey.svg),
    url(@/assets/images/register-form-gradient-star.svg);
  background-blend-mode: hard-light;
  background-repeat: no-repeat;
}
.reg-suc__modal__title {
  color: #fff;
  text-align: center;
  font-family: Montserrat;
  font-size: 32px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
  line-height: 3.4rem;
}
.reg-suc__modal__subtitle {
  color: #fff;
  text-align: center;
  font-family: Montserrat;
  font-size: 14px;
  font-style: normal;
  font-weight: 600;
  line-height: 1.6rem;
  /* background-position: 20px 19px;
  background-image: url("@/assets/images/wink-emoji-woman.svg");
  background-repeat: no-repeat; */
}
.reg-suc__modal__back-button {
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  font-weight: 400;
  line-height: normal;
  width: 100%;
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
  outline: none;
  border: none;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
}

@media (max-width: 950px) {
  .reg-suc__modal {
    width: 80%;
    height: auto;
    padding: 30px;
    gap: 30px;
  }
}
@media (max-width: 550px) {
  .reg-suc__modal {
    padding: 30px;
  }
  .reg-suc__modal__image {
    width: 100%;
  }
  .reg-suc__modal__image img {
    width: 100%;
  }
  .reg-suc__modal__title {
    font-size: 16px;
    line-height: normal;
  }
  .reg-suc__modal__subtitle {
    font-size: 12px;
    line-height: normal;
  }

}
</style>
