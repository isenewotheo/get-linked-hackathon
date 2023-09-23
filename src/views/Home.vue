<template>
  <div class="homepage">
    <Hero />
    <Introduction />
    <Guidelines />
    <Criteria />
    <Faq />
    <Timeline />
    <Prizes />
    <Partners />
    <PrivacyPolicy />
    <Footer />
  </div>
</template>

<script>
import Hero from "@/components/HomePage/Hero.vue";
import Introduction from "@/components/HomePage/Introduction.vue";
import Guidelines from "@/components/HomePage/Guidelines.vue";
import Criteria from "@/components/HomePage/Criteria.vue";
import Faq from "@/components/HomePage/Faq.vue";
import Timeline from "@/components/HomePage/Timeline.vue";
import Partners from "@/components/HomePage/Partners.vue";
import Prizes from "@/components/HomePage/Prizes.vue";
import PrivacyPolicy from "@/components/HomePage/PrivacyPolicy.vue";
import Footer from "@/components/Footer.vue";

export default {
  components: {
    Hero,
    Introduction,
    Guidelines,
    Criteria,
    Faq,
    Timeline,
    Partners,
    Prizes,
    PrivacyPolicy,
    Footer,
  },
};
</script>

<style scoped>
.homepage {

  background-position: 0% 100px, 100% 300px;
  background-image: url(@/assets/images/Purple-Lens-Flare-PNG.png),
    url(@/assets/images/Purple-Lens-Flare-PNG.svg);
  background-blend-mode: hard-light;
  background-repeat: no-repeat;
  background-size: 760px 560px;
}
</style>
