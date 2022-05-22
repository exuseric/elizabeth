<template>
  <section class="content">
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
  name: 'ServicesSection',
  components: { ServiceCard },
}
</script>

<style lang="scss" scoped>
@use 'sass:math';

.content {
  @include content-grid;

  .card-grid,
  .content__header {
    grid-column: 1 / -1;
  }

  @include screen(large) {
    .content__header {
      grid-column: 2 / -2;
    }
  }
}

.content__header {
  padding: $spacing-lg 0;
  width: fit-content;

  h2 {
    font-size: scale('h1');
    font-weight: 900;
    letter-spacing: rem(0.1);
    text-transform: uppercase;
    line-height: 0.8;
    color: $primary-500;
  }
  @include screen-up(medium) {
    width: 100%;
  }
}

.card-grid {
  @include content-grid;
  height: fit-content;

  // padding: $spacing-lg 0;
  row-gap: $spacing-md;

  &__section {
    grid-column: 1 / -1;
  }

  @include screen(large) {
    &__section {
      grid-column: 2 / -2;
    }
  }
}

.card-grid__section {
  display: grid;
  grid-template-rows: rem(400) rem(400) auto;
  gap: $spacing-md;
  padding: $spacing-lg 0;

  @include screen(large) {
    $col-count: 4;
    $row-count: 6;

    width: 100%;
    height: fit-content;

    margin: auto;

    display: grid;
    grid-template-columns: repeat($col-count, math.div(55rem, $col-count));
    grid-template-rows: repeat($row-count, math.div(30rem, $row-count));
    justify-content: space-between;

    .card {
      grid-row: 2 / -1;
    }

    .card:nth-child(1) {
      grid-column: 1 / 3;
    }
    .card:nth-child(2) {
      grid-column: 3 / -1;
    }
    .title {
      @include center;
      width: fit-content;

      grid-row: 1 / 2;
      grid-column: 1 / -1;
      justify-self: end;
      z-index: 1;
    }
  }

  @include screen(x-large) {
    $col-count: 4;

    width: 100%;

    display: grid;
    grid-template-columns: repeat($col-count, math.div(81.25rem, $col-count));
    justify-content: space-between;
  }
}

.card-grid__section > .title {
  text-align: left;

  color: $neutral-500;

  padding: $spacing-md;

  font-size: scale('h3');
  font-weight: 900;
  text-transform: uppercase;
}
</style>
