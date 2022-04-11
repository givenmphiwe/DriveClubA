<template>
  <div v-show="!mobile" class="hero">
    <Navigation />
    <img src="../assets/hero-home.jpg" />

    <div class="goosebumps">GOOSEBUMPS</div>
    <div class="come">COME STANDARD</div>
    <div class="discover">
      Discover the benefits of DRIVECLUB Trade-in and get a free vehicle
      evaluation
    </div>

    <router-link :to="{ name: 'Contact' }">
      <div class="Contact-btn">
        <p class="Contact-us">Contact us</p>
        <div class="triangleTop"></div>
        <div class="triangleBottom"></div>
      </div>
    </router-link>
  </div>

  <!---Mobile----->
  <div v-show="mobile" class="Mobile-hero">
    <Navigation />
    <img src="../assets/hero-home.jpg" />

    <div class="Mobile-goosebumps">GOOSEBUMPS</div>
    <div class="Mobile-come">COME STANDARD</div>
    <div class="Mobile-discover">
      Discover the benefits of DRIVECLUB Trade-in and get a free vehicle
      evaluation
    </div>

    <router-link :to="{ name: 'Contact' }">
      <div class="Mobile-Contact-btn">
        <p class="Mobile-Contact-us">Contact us</p>
        <div class="Mobile-triangleTop"></div>
        <div class="Mobile-triangleBottom"></div>
      </div>
    </router-link>
  </div>

  <div v-show="!mobile" class="ferrari">
    <div class="image">
      <img src="../assets/car-1.jpg" />
    </div>

    <div class="La-fer">LA FERR</div>
    <div class="new">new range</div>
    <div class="La-fer2">LA FERRARI</div>
    <div>
      <router-link class="learn" :to="{ name: 'LearnMore' }"
        >Learn more</router-link
      >
    </div>
  </div>

  <!---Mobile---->
  <div v-show="mobile" class="Mobile-models">
    <div class="Mobile-image">
      <img src="../assets/car-2.jpg" />
    </div>
  </div>
  <div v-show="mobile" class="ModelBackground">
    <div class="Mobile-new">new range</div>
    <div class="Mobile-modelS">MODEL S</div>
    <div>
      <router-link class="Mobile-learn" :to="{ name: 'LearnMore' }"
        >Learn more <img src="../assets/chevron.svg"/></router-link
      >

    </div>
  </div>
  <!------>
  <div v-show="!mobile" class="models">
    <div class="image">
      <img src="../assets/car-2.jpg" />
    </div>

    <div class="Model">MODEL</div>
    <div class="new">new range</div>
    <div class="modelS">MODEL S</div>
    <div>
      <router-link class="learn" :to="{ name: 'LearnMore' }"
        >Learn more</router-link
      >
    </div>
  </div>

  <!--mobile-->
  <!---Mobile---->
  <div v-show="mobile" class="Mobile-models">
    <div class="Mobile-image">
      <img src="../assets/car-1.jpg" />
    </div>
  </div>
  <div v-show="mobile" class="ModelBackground">
    <div class="Mobile-new">new range</div>
    <div class="Mobile-modelS">LA FERRARI</div>
    <div>
      <router-link class="Mobile-learn" :to="{ name: 'LearnMore' }"
        >Learn more <img src="../assets/chevron.svg"/></router-link
      >

    </div>
  </div>
  <div type="footer">
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import Navigation from "../components/Navigation.vue";
import Footer from "../components/Footer.vue";

export default {
  name: "Home",
  components: { Navigation, Footer },

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
@import url("https://fonts.googleapis.com/css?family=Proxima+Nova");
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@700&display=swap");
@import "@/views/MobileStyle.scss";

.hero {
  background-attachment: fixed;
  position: relative;
  width: 1438px;
  height: 598px;

  img {
    object-fit: cover;
    height: 100%;
    width: 100%;
  }
  @media (max-width: 414px) {
    .img {
      width: 414px;
      height: 598px;
    }
  }

  .goosebumps {
    position: absolute;
    top: 172px;
    left: 140px;
    width: 714px;
    height: 91px;
    font: normal normal 800 80px/75px Proxima Nova;
    letter-spacing: 1.6px;
    color: #ffffff;
  }
  @media screen and (max-width: 414px) {
    .goosebumps {
      top: 185px;
      left: 32px;
      width: 344px;
      height: 54px;
      text-align: left;
      font: normal normal 800 48px/75px Proxima Nova;
      letter-spacing: 0.96px;
      color: #ffffff;
      text-transform: uppercase;
      opacity: 0.87;
    }
  }

  .come {
    position: absolute;
    top: 259px;
    left: 140px;
    height: 45px;
    /* UI Properties */
    font: normal normal 800 40px/38px Proxima Nova;
    letter-spacing: 1.6px;
    color: #ffffff;
    text-transform: uppercase;
    opacity: 0.87;
  }

  .discover {
    position: absolute;
    top: 332px;
    left: 140px;
    width: 466px;
    height: 45px;
    text-align: left;
    font: normal normal 300 16px/22px Poppins;
    letter-spacing: 0.32px;
    color: #ffffff;
    opacity: 0.6;
  }
  .triangleBottom {
    position: absolute;
    top: 34px;
    left: 0px;
    width: 11px;
    height: 11px;
    border-bottom: 11px solid #ff0050;
    border-right: 11px solid transparent;
  }

  .triangleTop {
    position: absolute;
    top: 0px;
    left: 142px;
    width: 11px;
    height: 11px;
    border-top: 11px solid #ff0050;
    border-left: 11px solid transparent;
  }
  .Contact-btn {
    position: absolute;
    top: 419px;
    left: 140px;
    width: 156px;
    height: 48px;
    /* UI Properties */
    background: #ff00504d 0% 0% no-repeat padding-box;
    border: 2px solid #ff0050;
    opacity: 1;
    text-decoration: none;
    &:hover {
      background-color: #ff0050;
    }

    .Contact-us {
      margin-top: 12px;
      text-align: center;
      font: normal normal medium 18px/21px Poppins;
      letter-spacing: 0.36px;
      color: #ffffff;
      opacity: 1;

      &:hover {
        background-color: #ff0050;
      }
    }
  }
}

.ferrari {
  height: 501px;
  width: 1438px;
  background-color: #161b1e;
  border-bottom: 2px solid white;
  border-top: 2px solid white;

  .image {
    position: absolute;
    left: 630px;
    width: 810px;
    height: 499px;
    //margin-left: 2px;
    border-left: 2px solid white;

    img {
      position: relative;
      height: 500px;
      /* UI Properties */
      opacity: 0.4;
      transition: 0.6s ease;

      &:hover {
        transform: scale(1.2);
      }
    }
  }

  .La-fer {
    margin-top: 103px;
    //left: 0.000034332275390625px;
    color: #14171a;
    font: normal normal Proxima Nova;
    font-size: 10em;
    font-weight: bolder;
    letter-spacing: 2.12px;
  }

  .new {
    position: absolute;
    top: 787px;
    margin-left: 140px;
    //width: 108px;
    height: 21px;
    text-align: left;
    font: normal normal normal 18px/75px Proxima Nova;
    letter-spacing: 0.72px;
    color: #ffffff;
    text-transform: uppercase;
    opacity: 0.6;
  }

  .La-fer2 {
    position: absolute;
    top: 830px;
    margin-left: 140px;
    height: 64px;
    text-align: left;
    font: normal normal 800 56px/75px Proxima Nova;
    letter-spacing: 1.12px;
    color: #ffffff;
    text-transform: uppercase;
    opacity: 0.87;
  }

  .learn {
    top: 20px;
    margin-left: 140px;
    width: 101px;
    height: 23px;
    text-align: left;
    text-decoration: none;
    font: normal normal normal 16px/25px Poppins;
    letter-spacing: 0.64px;
    color: #ff0050;
    opacity: 1;
  }
  .vertical-line {
    position: absolute;
    left: 630px;
    border-left: 2px solid white;
    height: 500px;
  }
}

.models {
  height: 501px;
  width: 1438px;
  background-color: #161b1e;
  border-bottom: 2px solid white;

  .image {
    position: absolute;
    border-right: 2px solid white;
    height: 499px;
    margin-left: 2px;

    img {
      position: relative;
      width: 810px;
      height: 501px;
      /* UI Properties */
      opacity: 0.4;
      transition: 0.6s ease;

      &:hover {
        transform: scale(1.2);
      }
    }
  }
  .Model {
    position: relative;
    top: 101px;
    margin-left: 812px;
    opacity: 1;
    color: #14171a;
    font: normal normal Proxima Nova;
    font-size: 10em;
    font-weight: bolder;
    letter-spacing: 5.12px;
  }

  .new {
    margin-top: 20px;
    margin-left: 976px;
    height: 21px;
    text-align: left;
    font: normal normal normal 18px/75px Proxima Nova;
    letter-spacing: 0.72px;
    color: #ffffff;
    text-transform: uppercase;
    opacity: 0.6;
  }

  .modelS {
    margin-top: 21px;
    margin-left: 976px;
    width: 250px;
    height: 64px;
    font: normal normal 800 56px/75px Proxima Nova;
    letter-spacing: 1.12px;
    color: #ffffff;
    text-transform: uppercase;
  }

  .learn {
    margin-top: 20px;
    margin-left: 976px;
    width: 101px;
    height: 23px;
    text-decoration: none;
    font: normal normal normal 16px/25px Poppins;
    letter-spacing: 0.64px;
    color: #ff0050;
    opacity: 1;
  }
}
</style>
