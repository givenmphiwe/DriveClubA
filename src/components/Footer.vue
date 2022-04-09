<template>
  <div class="footer">
    <nav>
      <div class="brand">
        <p>DRIVECLUB</p>
      </div>

      <div class="model">
        MODELS
        <ul>
          <li>
            <router-link class="link" :to="{ name: 'Home' }">la ferrari</router-link>
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
            <router-link class="link" :to="{ name: '' }"
              >Contact us</router-link
            >
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>
<script>
export default {};
</script>

<style lang="scss" scoped>
.footer {
  top: 1603px;
  left: -2px;
  width: 1442px;
  height: 264px;
  background: var(--grey-1000-elevation-) 0% 0% no-repeat padding-box;
  background: #22282d 0% 0% no-repeat padding-box;
  opacity: 1;

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
    margin-top: 80px;
    margin-left: 556.3px;
  }

  .more {
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
}
</style>
