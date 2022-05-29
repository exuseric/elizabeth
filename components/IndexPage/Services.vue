<template>
  <section class="content wrapper">
    <header class="content__header">
      <h2 class="mark">What I Do</h2>
    </header>
    <div class="card-grid">
      <div class="card-grid__section">
        <service-card
          title="Wedding"
          image="wedding.jpg"
          alt="wedding couple"
        />
        <service-card
          title="birthday"
          image="Birthday Celebration - 960x1440.jpg"
          alt="birthday celebration"
        />
        <p class="title mark">Look good &amp; feel good on your special days</p>
      </div>
      <div class="card-grid__section">
        <service-card
          title="photoshoot"
          image="pexels-media-946240-1651258348918.jpeg"
          alt="model posing"
        />
        <service-card
          title="videography"
          image="Behind The Scene of a Photoshoot - 1280x720.jpg"
          alt="birthday celebration"
        />
        <p class="title mark">On-Camera moments? I've got you covered!</p>
      </div>
    </div>
  </section>
</template>

<script>
import ServiceCard from './ServiceCard.vue'
export default {
  name: 'IndexPageServices',
  components: { ServiceCard },
}
</script>

<style lang="scss" scoped>
@use 'sass:math';

.content {
  margin: $section-padding-lg auto;

  .card-grid,
  .content__header {
    grid-column: 1 / -1;
  }

  @include screen(large) {
    .content__header {
      grid-column: 1 / -1;
    }
  }
}

.content__header {
  width: fit-content;

  h2 {
    font-size: scale('h3');
    font-weight: 900;
    letter-spacing: rem(0.1);
    text-transform: uppercase;
    line-height: 0.8;
    color: $neutral-500;
    width: fit-content;

    @include screen(x-large) {
      font-size: scale('h1');
    }
  }
  @include screen-up(medium) {
    text-align: center;
  }
}

.card-grid {
  @include content-grid;
  height: fit-content;

  padding: $spacing-lg 0;
  row-gap: $spacing-md;

  &__section {
    grid-column: 1 / -1;
  }
}

.card-grid__section {
  display: grid;
  grid-template-rows: rem(400) rem(400) auto;
  row-gap: $spacing-md;
  padding: $spacing-lg 0;

  @include screen(medium) {
    display: grid;
    grid-template-columns: 50% 50%;
    grid-template-rows: 75% 1fr;

    .card {
      grid-row: 1 / -1;
    }

    .title {
      grid-column: 1 / -1;
      align-self: end;
      height: fit-content;
    }
  }

  @include screen(medium) {
    height: rem(750);
  }
}

.card-grid__section > .title {
  width: fit-content;
  height: fit-content;

  text-align: left;

  color: $neutral-500;

  margin: auto;

  font-size: scale('h4');
  font-weight: 900;
  text-transform: uppercase;
}
</style>
