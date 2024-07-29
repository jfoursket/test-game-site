<script setup>

</script>

<template>
  <section class="section-hero">
    <div class="wrapper">
      <div class="hero">
        <h1 class="hero-title">
          awesome html5 games
          - NO MONEY!
        </h1>
        <h3 class="hero-subtitle">
          Your perfect place to get some
          fun and excitement
        </h3>
        <div class="hero-buttons">
          <button class="button button-none">Log in</button>
          <button class="button button-gradient">Play</button>
        </div>
        <div class="hero-form">
          <div class="hero-form-up">
            <div class="hero-form-up-title">Create a free account now</div>
            <div class="hero-form-up-right">
              <div class="hero-form-up-right-item">
                <img src="/src/assets/images/cubes.svg" alt="Cubes">
                <span>1000+ Games<br>Available</span>
              </div>
              <div class="hero-form-up-right-item">
                <img src="/src/assets/images/casino.svg" alt="Casino">
                <span>New game<br>Every week</span>
              </div>
              <div class="hero-form-up-right-item">
                <img src="/src/assets/images/timer.svg" alt="Timer">
                <span>Support our<br>users 24/7</span>
              </div>
            </div>
          </div>
          <form class="hero-form-form">
            <div class="hero-form-form-info">
              <input type="text" placeholder="Firstname" required>
              <input type="text" placeholder="lastname" required>
              <input type="email" placeholder="Email address" required>
              <button type="submit" class="button button-gradient hero-form-form-info-btn">Join now</button>
            </div>
            <div class="hero-form-form-privacy">
              <input type="checkbox" name="hero-privacy" id="hero-privacy" required>
              <label for="hero-privacy">I accept the Privacy Policy</label>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>