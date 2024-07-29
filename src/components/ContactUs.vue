<script setup>

</script>

<template>
  <section class="section-contact_us" id="contact_us">
    <div class="wrapper">
      <div class="contact_us">
       <div class="contact_us-info">
         <div class="contact_us-info-title">Contact us</div>
         <div class="contact_us-info-subtitle">If you have some questions, send us a message</div>
       </div>
        <form class="contact_us-form" id="contact_us-form">
          <div class="contact_us-form-inputs">
            <input class="input-form" type="text" placeholder="Firstname" required>
            <input class="input-form" type="email" placeholder="Email Address" required>
            <input class="input-form" type="text" placeholder="Your message here..." required>
          </div>
          <div class="contact_us-form-buttons">
            <div class="contact_us-form-buttons-privacy input-form-privacy">
              <input type="checkbox" name="contact_us-privacy" id="contact_us-privacy" required>
              <label for="contact_us-privacy">I accept the Privacy Policy</label>
            </div>
            <button type="submit" class="button button-gradient">Send</button>
          </div>
        </form>
      </div>
    </div>
  </section>
</template>