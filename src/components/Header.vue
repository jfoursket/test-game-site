<script setup>

</script>

<template>
  <header>
    <div class="wrapper">
      <div class="header">
        <div class="header-left">
          <a href="#" class="header-left-logo">
            <img alt="logo" class="logo" src="/src/assets/images/logo.svg" width="48" height="48"/>
          </a>
          <div class="header-left-nav">
            <a href="#games"
               :class="{'active': isActive('#games')}"
               @click.prevent="setActive('#games')">
              <span v-if="isActive('#games')" class="gradient-text">Games</span>
              <span v-else>Games</span>
            </a>
            <a href="#contact_us"
               :class="{'active': isActive('#contact_us')}"
               @click.prevent="setActive('#contact_us')">
              <span v-if="isActive('#contact_us')" class="gradient-text">Contact Us</span>
              <span v-else>Contact Us</span>
            </a>
            <a href="#footer"
               :class="{'active': isActive('#footer')}"
               @click.prevent="setActive('#footer')">
              <span v-if="isActive('#footer')" class="gradient-text">Terms of Use</span>
              <span v-else>Terms of Use</span>
            </a>
            <a href="#about"
               :class="{'active': isActive('#about')}"
               @click.prevent="setActive('#about')">
              <span v-if="isActive('#about')" class="gradient-text">About</span>
              <span v-else>About</span>
            </a>
          </div>
        </div>
        <div class="header-buttons">
          <button class="button">Sign up</button>
          <button class="button button-gradient">Log in</button>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      activeLink: window.location.hash || '#about'
    };
  },
  methods: {
    setActive(link) {
      this.activeLink = link;
      window.location.hash = link;
    },
    isActive(link) {
      return this.activeLink === link;
    },
    updateActiveLink() {
      this.activeLink = window.location.hash || '#about';
    }
  },
  mounted() {
    window.addEventListener('hashchange', this.updateActiveLink);
  },
  beforeDestroy() {
    window.removeEventListener('hashchange', this.updateActiveLink);
  }
}
</script>