<template>
  <header :class="{ 'scrolled-nav': scrollPosition }">
    <nav>
      <div class="branding">
        <img src="../assets/images/img_logo_dtt@3x.png" alt="" />
      </div>
      <ul v-show="!mobile" class="navigation">
        <li>
          <router-link class="link" :to="{ name: 'home' }">Houses</router-link>
        </li>
        <li>
          <router-link class="link" :to="{ name: 'about' }">About</router-link>
        </li>
      </ul>
      <div class="icon">
        <i
          @click="toggleMobileNav"
          v-show="mobile"
          class="far fa-bars"
          :class="{ 'icon-active': mobileNav }"
        ></i>
      </div>
      <transition name="mobile-nav">
        <ul v-show="mobileNav" class="dropdown-nav">
          <li>
            <router-link class="link" :to="{ name: 'Home' }"
              >Houses</router-link
            >
          </li>
          <li>
            <router-link class="link" :to="{ name: 'about' }"
              >About</router-link
            >
          </li>
        </ul>
      </transition>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Navigation",
  data() {
    return {
      scrollPosition: null,
      mobile: null,
      mobileNav: null,
      windowWidth: null,
    };
  },
  methods: {
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav;
    },
  },
};
</script>

<style lang="scss" scoped>
header {
  background-color: #fff;
  z-index: 99;
  width: 100%;
  position: fixed;
  transition: 0.5s ease all;
  color: #fff;
}

nav {
  position: relative;
  display: flex;
  color: #eb5440;
  flex-direction: row;
  padding: 12px 0;
  transition: 0.5s ease all;
  width: 100%;
  margin: 0 auto;
  @media (min-width: 2000px) {
    max-width: 2000px;
  }

  ul,
  .link {
    font-weight: 500;
    color: black;
    list-style: none;
    text-decoration: none;
  }

  li {
    text-transform: uppercase;
    padding: 16px;
    margin-left: 16px;
  }

  .link {
    font-size: 14px;
    transition: 0.5s ease all;
    padding-bottom: 4px;
    border-bottom: 1px solid transparent;
    font-family: "MontserratBold";

    &:hover {
      color: #eb5440;
      border-color: #fff;
    }
  }

  .branding {
    display: flex;
    align-items: center;

    img {
      width: 100px;
      transition: 0.5s ease all;
      margin-left: 120px;
    }
  }

  .navigation {
    display: flex;
    align-items: center;
    flex: 1;
    justify-content: flex-start;
  }

  .icon {
    display: flex;
    position: absolute;
    top: 0;
    right: 24px;
    height: 100%;
    i {
      cursor: pointer;
      font-size: 24px;
      transition: 0.5s ease all;
    }
  }

  .icon-active {
    transform: rotate(180deg);
  }
  .dropdown-nav {
    display: flex;
    flex-direction: column;
    position: fixed;
    width: 100%;
    max-width: 250px;
    height: 100%;
    background-color: #fff;
    top: 0;
    left: 0;

    li {
      margin-left: 0;
      .link {
        color: #000;
      }
    }
  }
}
</style>