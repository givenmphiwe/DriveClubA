<template>
  <div v-show="!mobile" class="footer">
    <nav>
      <div class="brand">
        <img class="logo" src="../assets/logo.svg" />
        <p class="copyright">&copy; Driveclub. All rights reserved</p>
      </div>

      <div class="model">
        MODELS
        <ul>
          <li>
            <router-link class="link" :to="{ name: '' }">la ferrari</router-link
            >
          </li>
          <li>
            <router-link class="link" :to="{ name: '' }">model s</router-link>
          </li>
        </ul>
      </div>

      <div class="more">
        MORE
        <ul>
          <li>
            <router-link class="link" :to="{ name: 'Home' }">Home</router-link>
          </li>
          <li>
            <router-link class="link" :to="{ name: 'Contact' }"
              >Contact us</router-link
            >
          </li>
        </ul>
      </div>

      <div class="icon">
        <a href=""><img class="facebook" src="../assets/facebook.svg" /></a>
        <a href=""><img class="instagram" src="../assets/instagram.svg" /></a>
        <a href=""><img class="twitter" src="../assets/twitter.svg" /></a>
        <a href=""><img class="linkedin" src="../assets/linkedin.svg" /></a>
        <a href=""><img class="youtube" src="../assets/youtube.svg" /></a>
      </div>
    </nav>
  </div>

  <!---Mobile Foooter--->
  <div v-show="mobile" class="Mobile-footer">
    <nav>
      <div class="Mobile-brand">
        <img src="../assets/logo.svg" />
        <p class="Mobile-copyright">&copy; Driveclub. All rights reserved</p>
      </div>

      <div class="Mobile-model">
        MODELS
        <ul>
          <li>
            <router-link class="Mobile-link" :to="{ name: '' }">la ferrari</router-link
            >
          </li>
          <li>
            <router-link class="Mobile-link" :to="{ name: '' }">model s</router-link>
          </li>
        </ul>
      </div>

      <div class="Mobile-more">
        MORE
        <ul>
          <li>
            <router-link class="Mobile-link" :to="{ name: 'Home' }">Home</router-link>
          </li>
          <li>
            <router-link class="Mobile-link" :to="{ name: 'Contact' }"
              >Contact us</router-link
            >
          </li>
        </ul>
      </div>

      <div class="Mobile-icon">
        <a href=""><img class="Mobile-facebook" src="../assets/facebook.svg" /></a>
        <a href=""><img class="Mobile-instagram" src="../assets/instagram.svg" /></a>
        <a href=""><img class="Mobile-twitter" src="../assets/twitter.svg" /></a>
        <a href=""><img class="Mobile-linkedin" src="../assets/linkedin.svg" /></a>
        <a href=""><img class="Mobile-youtube" src="../assets/youtube.svg" /></a>
      </div>
    </nav>
  </div>
</template>
<script>
export default {
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
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@700&display=swap');
@import '@/components/MobileFooter.scss';


.footer {
  top: 1603px;
  left: -2px;
  width: 1442px;
  height: 264px;
  background: grey 0% 0% no-repeat padding-box;
  background: #22282d 0% 0% no-repeat padding-box;
  opacity: 1;

  .logo {
    width: 148px;
    height: 16px;
    opacity: 1;
  }
  nav {
    position: relative;
    color: #fff;
    flex-direction: row;
    display: flex;
  }

  .brand {
    margin-top: 80px;
    margin-left: 185.09px;
  }

  .model {
    height: 23px;
    font: normal normal 600 16px/25px Poppins;
    letter-spacing: 1.28px;
    color: #ffffff;
    opacity: 1;
    margin-top: 80px;
    margin-left: 556.3px;
  }

  .more {
    height: 23px;
    font: normal normal 600 16px/25px Poppins;
    letter-spacing: 1.28px;
    color: #ffffff;
    opacity: 1;
    margin-top: 80px;
    margin-left: 134px;
  }

  ul,
  .link {
    list-style: none;
    text-decoration: none;
    margin-top: 18px;
    text-align: left;
    font: normal normal 300 15px/23px Poppins;
    letter-spacing: 1.2px;
    color: #ffffff;
    opacity: 0.6;
  }

  li {
    text-transform: uppercase;
  }

  .link {
    font-size: 14px;
    transition: 0.5s ease all;
    padding-bottom: 4px;
    border-bottom: 1 pc solid transparent;

    &:hover {
      color: #ff0050;
      border-color: #ff0050;
    }
  }

  .copyright {
    margin-top: 12px;
    text-align: left;
    font: normal normal 300 14px/21px Poppins;
    letter-spacing: 0.56px;
    color: #ffffff;
    opacity: 0.48;
  }

  .icon {
    top: 164px;
    left: 184px;
    position: absolute;
    flex-direction: row;
    display: flex;

    .facebook {
      width: 10px;
      height: 20px;
    }

    .instagram {
      width: 20px;
      height: 20px;
      margin-left: 25px;
    }

    .twitter {
      width: 25px;
      height: 20px;
      margin-left: 25.38px;
    }

    .linkedin {
      width: 20px;
      height: 20px;
      margin-left: 26.25px;
    }

    .youtube {
      width: 29px;
      height: 20px;
      margin-left: 20px;
    }
  }
}
</style>
