<template>
  <div v-show="!mobile" class="LearnPage">
    <img class="Image" src="../assets/car-large.jpg" />

    <div class="NewRange">New Range</div>
    <div class="LaFerr">LA FERRARI</div>
    <div class="lorem">Lorem ipsum dolor sit amet consectetur adipisicing elit. Mollitia placeat nam ipsa, deleniti quam asperiores est, voluptatibus nulla non molestias natus dolorem minus cumque inventore perspiciatis sed nemo! Ad, saepe! Loe
        <br>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptas, ullam quia! Quod hic repudiandae accusamus velit voluptatum repellendus sit harum consequatur vitae pariatur tempore, incidunt esse. Reprehenderit earum veniam natus?
        <br><br>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Autem in, architecto consectetur id atque quis eius praesentium neque dolore voluptatibus beatae harum, eum laboriosam laudantium quae recusandae, aperiam omnis suscipit?
        Lorem ipsum dolor sit amet consectetur adipisicing elit.
    </div>
  </div>



  <div v-show="mobile" class="Mobile-LearnPage">
    <img class="Mobile-Image" src="../assets/car-large.jpg" />

    
  </div>

  <div v-show="mobile" class="Details">
    <div class="Mobile-NewRange">New Range</div>
    <div class="Mobile-LaFerr">LA FERRARI</div>
    <div class="Mobile-lorem">Lorem ipsum dolor sit amet consectetur adipisicing elit. Mollitia placeat nam ipsa, deleniti quam asperiores est, voluptatibus nulla non molestias natus dolorem minus cumque inventore perspiciatis sed nemo! Ad, saepe! Loe
        <br>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptas, ullam quia! Quod hic repudiandae accusamus velit voluptatum repellendus sit harum consequatur vitae pariatur tempore, incidunt esse. Reprehenderit earum veniam natus?
        <br><br>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Autem in, architecto consectetur id atque quis eius praesentium neque dolore voluptatibus beatae harum, eum laboriosam laudantium quae recusandae, aperiam omnis suscipit?
        Lorem ipsum dolor sit amet consectetur Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt quia odio culpa necessitatibus vero alias hic id nihil quo, voluptatibus voluptatem, neque officiis praesentium maiores. Deserunt, nemo. Dignissimos, sapiente quod.
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Earum maiores alias iure. Nesciunt quibusdam debitis eius totam sit? Blanditiis ratione facilis delectus rerum nulla tempora accusamus et repudiandae debitis deleniti.
    </div>
  </div>
</template>

<script>
export default {
  name: "LearnMore",
  data() {
    return {
      scrolledNav: null,
      mobile: null,
      mobileNav: null,
      windowWidth: null,
    };
  },
  created() {
    window.addEventListener("resize", this.checkScreen);
    this.checkScreen;
  },
  //
  methods: {
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav;
    },

    updateScroll() {
      const scrollPosition = window.scrollY;
      if (scrollPosition > 50) {
        this.scrolledNav = true;
        return;
      }
      this.scrolledNav = false;
    },

    checkScreen() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 750) {
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
      return;
    },
  },

};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@700&display=swap");
@import '@/views/MobileLearn.scss';

.LearnPage {
  background: #171b1e;
  width: 1440px;
  height: 820px;
 
  img {
    width: 810px;
    height: 820px;
    background: #161b1e 0% 0% no-repeat padding-box;
  }

  .NewRange {
    position: absolute;
    top: 90px;
    left: 890px;
    height: 21px;
    text-align: left;
    font: normal normal normal 18px/75px Proxima Nova;
    letter-spacing: 0.72px;
    color: #ffffff;
    text-transform: uppercase;
    opacity: 0.6;
  }

  .LaFerr {
    position: absolute;
    top: 121px;
    left: 890px;
    width: 325px;
    height: 64px;
    text-align: left;
    font: normal normal 800 56px/75px Proxima Nova;
    letter-spacing: 1.12px;
    color: #ffffff;
    text-transform: uppercase;
    opacity: 0.87;
  }

  .lorem {
    position: absolute;
    top: 245px;
    left: 890px;
    width: 470px;
    
    text-align: left;
    font: normal normal 300 18px/27px Poppins;
    letter-spacing: 0.36px;
    color: #ffffff;
    opacity: 0.87;
  }
}
</style>