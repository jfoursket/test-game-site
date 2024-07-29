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
        <form class="contact_us-form">
          <div class="contact_us-form-inputs">
            <input class="input-form" type="text" placeholder="Firstname">
            <input class="input-form" type="email" placeholder="Email Address">
            <input class="input-form" type="text" placeholder="Your message here...">
          </div>
          <div class="contact_us-form-buttons">
            <div class="contact_us-form-buttons-privacy input-form-privacy">
              <input type="checkbox" name="contact_us-privacy" id="contact_us-privacy">
              <label for="contact_us-privacy">I accept the Privacy Policy</label>
            </div>
            <button class="button button-gradient">Send</button>
          </div>
        </form>
      </div>
    </div>
  </section>
</template>