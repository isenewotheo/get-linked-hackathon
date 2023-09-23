<template>
  <section class="container">
    <div class="privacy-policy">
      <div class="privacy-policy__content">
        <div class="privacy-policy__content__header">
          Privacy Policy and
          <div style="color: #d434fe">Terms</div>
        </div>
        <div class="privacy-policy__content__date">
          Last updated on September 12, 2023
        </div>
        <div class="privacy-policy__content__info">
          Below are our privacy & policy, which outline a lot of goodies. <br />
          it’s our aim to always take of our participant
        </div>
        <div class="privacy-policy__content__card">
          <div class="privacy-policy__content__card__text">
            At getlinked tech Hackathon 1.0, we value your privacy and are
            committed to protecting your personal information. This Privacy
            Policy outlines how we collect, use, disclose, and safeguard your
            data when you participate in our tech hackathon event. By
            participating in our event, you consent to the practices described
            in this policy.
          </div>
          <div class="privacy-policy__content__license">
            <div class="privacy-policy__content__license__title">
              Licensing Policy
            </div>
            <div class="privacy-policy__content__license__subtitle">
              Here are terms of our Standard License:
            </div>
            <ul class="privacy-policy__content__license__list">
              <li>
                <img src="@/assets/images/list-terms-check.svg" alt="" />
                <div>
                  The Standard License grants you a non-exclusive right to
                  navigate and register for our event:
                </div>
              </li>
              <li>
                <img src="@/assets/images/list-terms-check.svg" alt="" />
                <div>
                  You are licensed to use the item available at any free source
                  sites, for your project developement
                </div>
              </li>
            </ul>
          </div>
          <button class="privacy-policy__read-more__button">Read More</button>
        </div>
      </div>
      <div class="privacy-policy__image">
        <img
          src="@/assets/images/privacy-policy-shield-icon.svg
"
          class="privacy-policy__image__shield-image"
        />
        <img
          src="@/assets/images/privacy-policy-boy-with-key-and-lock.svg"
          class="privacy-policy__image__key-and-lock-image"
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.privacy-policy {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  padding: 50px 20px;
  /* height: fit-content; */
  width: 100%;

  font-size: 14px;

  background-position: 350px 30px, 100% 90%, 600px 140px, 70% 700px, 90% 220px,
    67% 82%, 0px 90%;
  background-image: url(@/assets/images/register-form-star-lightgrey.svg),
    url(@/assets/images/register-form-star-lightgrey.svg),
    url(@/assets/images/register-form-purple-star.svg),
    url(@/assets/images/register-form-small-gradient-star.svg),
    url(@/assets/images/register-form-small-star.svg),
    url(@/assets/images/register-form-small-star.svg),
    url(@/assets/images/register-form-purple-star.svg);
  background-blend-mode: hard-light;
  background-repeat: no-repeat;


  padding-top: 93px;
  padding-bottom: 161px;
}
.privacy-policy__content__header {
  color: #fff;
  font-family: Clash Display;
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  margin-bottom: 17px;
}
.privacy-policy__content__date {
  color: rgba(255, 255, 255, 0.75);
  font-family: Montserrat;
  
  font-style: normal;
  font-weight: 400;
  line-height: 27.5px;
  margin-bottom: 30px;
}

.privacy-policy__content__info {
  color: #fff;
  font-family: Montserrat;
  
  font-style: normal;
  font-weight: 400;
  line-height: 26.376px;
  margin-bottom: 69px;
}

.privacy-policy__content__card {
  padding: 59px 72px;
  width: 569px;
  /* height: 608px; */
  flex-shrink: 0;
  border-radius: 5px;
  border: 1px solid #d434fe;
  background: rgba(217, 217, 217, 0.03);
}

.privacy-policy__content__card__text {
  color: #fff;
  font-family: Montserrat;
  
  font-style: normal;
  font-weight: 400;
  line-height: 30.296px;
  margin-bottom: 24px;
}

.privacy-policy__content__license__title {
  color: #d434fe;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 700;
  line-height: 34.624px;
}

.privacy-policy__content__license__subtitle {
  color: #fff;
  font-family: Montserrat;
  
  font-style: normal;
  font-weight: 700;
  line-height: 30.296px;

  margin-bottom: 18px;
}

.privacy-policy__content__license__list {
  display: flex;
  flex-direction: column;
  list-style: none;
  gap: 18px;
  margin-bottom: 19px;
}
.privacy-policy__content__license__list li {
  color: #fff;
  font-family: Montserrat;
  
  font-style: normal;
  font-weight: 400;
  line-height: 30.296px;
  display: flex;
  align-items: flex-start;
  gap: 14px;
}
.privacy-policy__content__license__list li img {
  margin-top: 8px;
}
.privacy-policy__read-more__button {
  margin: auto;
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  font-weight: 400;
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
  width: 172px;
  height: 53px;
}

.privacy-policy__image {
  width: 559px;
  height: fit-content;
  position: relative;
  height: 1000px;
}
.privacy-policy__image img {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
}
.privacy-policy__image__shield-image {
  left: 20px;
  top: -120px;
}
.privacy-policy__image__key-and-lock-image {
  left: 0px;
  top: 80px;
}

@media (max-width: 1280px) {
  .privacy-policy {
    display: block;
    text-align: center;
    font-size: 12px;
  }
  .privacy-policy__content__card,
  .privacy-policy__image {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .privacy-policy__image {
    margin-top: 160px;
  }
  .privacy-policy__content__license__list li {
    text-align: left;
  }
}

@media (max-width: 800px) {
    .privacy-policy {

    font-size: 12px;
    }
  .privacy-policy__content__card {
    padding: 45px 15px;
  }
  .privacy-policy__content__header {
    font-size: 20px;
  }
}
@media (max-width: 600px) {
  .privacy-policy__image {
    margin-top: 20px;
  }
}
</style>
