<script setup>
import {ref, onMounted} from 'vue';
import Header from "@/components/Header.vue";
import Hero from "@/components/Hero.vue";
import Games from "@/components/Games.vue";
import ContactUs from "@/components/ContactUs.vue";
import Footer from "@/components/Footer.vue";
import PopUp from "@/components/PopUp.vue";
import Preloader from "@/components/Preloader.vue";

const isPopUpOpen = ref(false);

function togglePopUp() {
  isPopUpOpen.value = !isPopUpOpen.value;
}

function closePopUp() {
  isPopUpOpen.value = false;
}

const isLoading = ref(true);
function hidePreloader() {
  isLoading.value = false;
}

// Рабочий
// onMounted(() => {
//   if (document.readyState === 'complete') {
//     hidePreloader();
//   } else {
//     window.addEventListener('DOMContentLoaded', hidePreloader);
//     window.addEventListener('load', hidePreloader);
//   }
// });

// Для демонстрации
onMounted(() => {
  setTimeout(() => {
    isLoading.value = false;
  }, 1000);
});
</script>

<template>
  <Preloader v-if="isLoading"/>
  <Header :togglePopUp="togglePopUp"/>


  <main :class="{ 'open-pop-up': isPopUpOpen }">
    <PopUp :closePopUp="closePopUp"/>
    <Hero :togglePopUp="togglePopUp"/>
    <Games :togglePopUp="togglePopUp"/>
    <ContactUs/>
  </main>

  <Footer/>
</template>

<script>

</script>
