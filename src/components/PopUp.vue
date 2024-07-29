<script setup>
import { defineProps } from 'vue';

const props = defineProps(['closePopUp']);
</script>

<template>
  <div class="pop_up-background" @click="props.closePopUp"></div>
  <div class="pop_up" @click.stop>
    <div class="pop_up-tabs">
      <a
          class="pop_up-tabs-item"
          :class="{ active: isSignUpActive }"
          @click="setActiveTab('signUp')">Sign Up</a>
      <a
          class="pop_up-tabs-item"
          :class="{ active: !isSignUpActive }"
          @click="setActiveTab('login')">Login</a>
    </div>
    <form class="pop_up-form">
      <div v-if="isSignUpActive" class="pop_up-form-inputs">
        <input type="text" class="input-form" placeholder="Firstname" required>
        <input type="text" class="input-form" placeholder="Lastname" required>
        <input type="email" class="input-form" placeholder="Email" required>
        <div class="pop_up-form-inputs-pass">
          <input type="password" class="input-form" placeholder="Password" required>
          <input type="password" class="input-form" placeholder="Confirm Password" required>
        </div>
      </div>
      <div v-else class="pop_up-form-inputs">
        <input type="email" class="input-form" placeholder="Email" required>
        <div class="pop_up-form-inputs-pass">
          <input type="password" class="input-form" placeholder="Password" required>
        </div>
      </div>
      <div class="pop_up-form-privacy input-form-privacy">
        <input type="checkbox" name="pop_up-privacy" id="pop_up-privacy" required>
        <label for="pop_up-privacy">I accept the <a href="#">Privacy Policy</a></label>
      </div>
      <button v-if="isSignUpActive" type="submit" class="pop_up-form-button button button-gradient">Join Now</button>
      <button v-else type="submit" class="pop_up-form-button button button-gradient">Login</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isSignUpActive: true
    };
  },
  methods: {
    setActiveTab(tab) {
      this.isSignUpActive = (tab === 'signUp');
    }
  }
}
</script>