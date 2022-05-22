<template>
  <article class="card">
    <div class="card__image">
      <nuxt-img
        fit="cover"
        format="webp"
        quality="80"
        width="400"
        height="400"
        :src="`/images/services/${image}`"
        :alt="alt"
      />
    </div>
    <header class="card__header">
      <h3>
        {{ title }}
      </h3>
    </header>
  </article>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Title',
    },
    alt: {
      type: String,
      default: 'service',
    },
    image: {
      type: String,
      default: 'african-art.jpg',
    },
  },
}
</script>

<style lang="scss" scoped>
.card {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  grid-template-rows: repeat(12, 1fr);

  &__image {
    grid-column: 1 / -1;
    grid-row: 1 / -1;
  }

  &__header {
    grid-column: 1 / span 3;
    grid-row: 4 / span 3;
    z-index: 2;
  }
}

.card {
  width: 100%;
  height: 100%;

  // border: rem(10) solid $primary-50;
  background-color: transparent;
}

.card__header {
  @include center;
  display: none;

  color: $neutral-50;
  background-color: $neutral-900;

  padding: $spacing-sm;

  h3 {
    font-size: scale('h3');
    font-weight: 100;
    line-height: 1.125;
    text-transform: uppercase;
    text-align: left;
  }
}
</style>
