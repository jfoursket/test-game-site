<script setup>
import { defineProps, ref, onMounted, onBeforeUnmount } from 'vue';

const props = defineProps(['togglePopUp']);
const isNavOpen = ref(false);
const activeLink = ref(window.location.hash || '#about');

function handleClick() {
  if (isNavOpen.value) {
    closeNav();
  }
  props.togglePopUp();
}

function closeNav() {
  isNavOpen.value = false;
}

function toggleNav() {
  isNavOpen.value = !isNavOpen.value;
}

function setActive(link) {
  activeLink.value = link;
  window.location.hash = link;
}

function isActive(link) {
  return activeLink.value === link;
}

function updateActiveLink() {
  activeLink.value = window.location.hash || '#about';
}

onMounted(() => {
  window.addEventListener('hashchange', updateActiveLink);
});

onBeforeUnmount(() => {
  window.removeEventListener('hashchange', updateActiveLink);
});
</script>

<template>
  <header>
    <div class="wrapper">
      <div class="header">
        <div class="header-left">
          <a href="#" class="header-left-logo">
            <img alt="logo" class="logo" src="/src/assets/images/logo.svg" width="48" height="48"/>
          </a>
          <div :class="{'header-left-nav': true, 'nav-open': isNavOpen}">
            <a href="#games"
               :class="{'active': isActive('#games')}"
               @click.prevent="setActive('#games')" @click="closeNav">
              <span v-if="isActive('#games')" class="gradient-text">Games</span>
              <span v-else>Games</span>
            </a>
            <a href="#contact_us"
               :class="{'active': isActive('#contact_us')}"
               @click.prevent="setActive('#contact_us')" @click="closeNav">
              <span v-if="isActive('#contact_us')" class="gradient-text">Contact Us</span>
              <span v-else>Contact Us</span>
            </a>
            <a href="#footer"
               :class="{'active': isActive('#footer')}"
               @click.prevent="setActive('#footer')" @click="closeNav">
              <span v-if="isActive('#footer')" class="gradient-text">Terms of Use</span>
              <span v-else>Terms of Use</span>
            </a>
            <a href="#about"
               :class="{'active': isActive('#about')}"
               @click.prevent="setActive('#about')" @click="closeNav">
              <span v-if="isActive('#about')" class="gradient-text">About</span>
              <span v-else>About</span>
            </a>
          </div>
        </div>
        <div class="header-buttons">
          <button class="button" @click="handleClick">Sign up</button>
          <button class="button button-gradient" @click="handleClick">Log in</button>
        </div>
        <div class="burger-menu" @click="toggleNav">
          <div class="line"></div>
          <div class="line"></div>
          <div class="line"></div>
        </div>
      </div>
    </div>
  </header>
  <div v-if="isNavOpen" class="pop_up-background nav-open" @click="closeNav"></div>
</template>