<script setup>
import {ref} from 'vue';
import Header from "@/components/Header.vue";
import Hero from "@/components/Hero.vue";
import Games from "@/components/Games.vue";
import ContactUs from "@/components/ContactUs.vue";
import Footer from "@/components/Footer.vue";
import PopUp from "@/components/PopUp.vue";

const isPopUpOpen = ref(false);

function togglePopUp() {
  isPopUpOpen.value = !isPopUpOpen.value;
}

function closePopUp() {
  isPopUpOpen.value = false;
}
</script>

<template>
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
