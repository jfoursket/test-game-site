<script setup>
import {defineProps} from 'vue';

const props = defineProps(['togglePopUp']);

function handleClick() {
  props.togglePopUp();
}
</script>

<template>
  <section class="section-games">
    <div class="wrapper">
      <div class="games">
        <div class="games-up">
          <div class="games-up-title">Our Games</div>
          <div class="games-up-subtitle">
            <span>Get Virtual Welcome bonus after Sign Up</span>
            <a href="#">All games</a>
          </div>
        </div>
        <div class="games-cards">
          <div class="games-cards-small">
            <a class="games-cards-small-item">
              <img src="/src/assets/images/gametype1.png" alt="Game">
              <div class="games-cards-small-item-text">
                <p class="games-cards-small-item-text-name">Double Jackpot</p>
                <span class="games-cards-small-item-text-corp">NetentGames</span>
              </div>
            </a>
            <a class="games-cards-small-item">
              <img src="/src/assets/images/gametype2.png" alt="Game">
              <div class="games-cards-small-item-text">
                <p class="games-cards-small-item-text-name">All Aboard: Dynam...</p>
                <span class="games-cards-small-item-text-corp">RushGameStudio</span>
              </div>
            </a>
            <a class="games-cards-small-item">
              <img src="/src/assets/images/gametype3.png" alt="Game">
              <div class="games-cards-small-item-text">
                <p class="games-cards-small-item-text-name">Book Of Tombs</p>
                <span class="games-cards-small-item-text-corp">NetentGames</span>
              </div>
            </a>
            <a class="games-cards-small-item">
              <img src="/src/assets/images/gametype4.png" alt="Game">
              <div class="games-cards-small-item-text">
                <p class="games-cards-small-item-text-name">Rudolph’s Ride</p>
                <span class="games-cards-small-item-text-corp">NetentGames</span>
              </div>
            </a>
            <a class="games-cards-small-item">
              <img src="/src/assets/images/gametype5.png" alt="Game">
              <div class="games-cards-small-item-text">
                <p class="games-cards-small-item-text-name">Starburst XXXtreme</p>
                <span class="games-cards-small-item-text-corp">StarBurst Inc.</span>
              </div>
            </a>
            <a class="games-cards-small-item">
              <img src="/src/assets/images/gametype6.png" alt="Game">
              <div class="games-cards-small-item-text">
                <p class="games-cards-small-item-text-name">Black Diamond</p>
                <span class="games-cards-small-item-text-corp">RushGameStudio</span>
              </div>
            </a>
          </div>
          <div class="games-cards-big">
            <div class="games-cards-big-short">
              <div class="games-cards-big-short-item">
                <div class="games-cards-big-short-item-text">
                  <p class="games-cards-big-short-item-text-name">Dynamite Riches Megaways</p>
                  <span class="games-cards-big-short-item-text-desc">Miners revealed a gain of €46,672 for Sandra M.! You too, dynamite the reels of the Red Tiger Daily Jackpot machines</span>
                </div>
                <button class="button button-small games-cards-big-short-item-btn" @click="togglePopUp">Play now
                </button>
              </div>
              <div class="games-cards-big-short-item">
                <div class="games-cards-big-short-item-text">
                  <p class="games-cards-big-short-item-text-name">Gator Gold Deluxe Gigablox</p>
                  <span class="games-cards-big-short-item-text-desc">These swamps conceal many dangers but especially precious treasures. Will you be able to find them?</span>
                </div>
                <button class="button button-small games-cards-big-short-item-btn" @click="togglePopUp">Play now
                </button>
              </div>
            </div>
            <div class="games-cards-big-item">
              <img src="/src/assets/images/long-gametype1.png" alt="Game">
              <div class="games-cards-big-item-info">
                <div class="games-cards-big-item-info-text">
                  <p class="games-cards-big-item-info-text-name">Our deals are not to be missed</p>
                  <span class="games-cards-big-item-info-text-desc">Discover a wide range of weekly promotions</span>
                </div>
                <button class="button button-small" @click="togglePopUp">Read more</button>
              </div>
            </div>
          </div>
        </div>
        <div class="games-info">* We don't offer opportunities to play for real money. Our games are free demo. All
          games were invented for entertainment purposes only and do not offer real money prizes.
        </div>
      </div>
    </div>
  </section>
</template>