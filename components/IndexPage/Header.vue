<template>
  <header class="hero">
    <section class="hero__content">
      <article class="title">
        <div class="title__heading">
          <h1 class="name mark">Elizabeth Nthena <br />Makeup Artist</h1>
          <h2 class="work">
            Let's express who you are on the inside with limitless possibilities
          </h2>
        </div>
        <div class="title__contact">
          <nuxt-link to="/contact" class="contact__btn primary-btn">
            Let's Work Together
          </nuxt-link>

          <nuxt-link to="/gallery" class="sec-btn gallery-btn">
            Browse Gallery
          </nuxt-link>
        </div>
      </article>
      <div class="image">
        <nuxt-img
          fit="contain"
          quality="100"
          format="webp"
          width="1268"
          height="1972"
          src="/images/header/main-header.png"
          alt="composite of a woman with flowers on a red circle backdrop"
        />
      </div>
    </section>
  </header>
</template>

<script>
export default {
  name: 'IndexPageHeader',
}
</script>

<style lang="scss" scoped>
.hero {
  position: relative;
  z-index: 1;

  // min-height: 40rem;
  height: fit-content;

  background: $neutral-50;
  overflow-x: hidden;

  @include screen('large') {
    @include center;
    padding: $spacing-md 0;
    // min-height: 60rem;
  }

  @include screen('x-large') {
    @include center;
    // min-height: 70rem;
  }
}

.hero__content {
  height: fit-content;

  @include screen('large') {
    @include content-grid;
    .title {
      grid-column: 1 / 7;
      grid-row: 1 / -1;
    }
    .image {
      grid-column: 8 / -1;
      grid-row: 1 / -1;
    }
  }
}

.title {
  @include content-grid;
  row-gap: 2.25rem;

  padding: $spacing-lg 0;

  &__heading {
    grid-column: 1 / -1;
    justify-self: center;
    align-self: center;
  }

  &__contact {
    grid-column: 1 / -1;
  }

  @include screen(medium) {
    row-gap: 2.25rem;
  }

  @include screen('large') {
    max-width: 100%;
    display: block;
  }
}

.name {
  font-size: scale('h4');
  font-weight: 600;

  color: $neutral-900;

  margin: $spacing-md 0;
  width: fit-content;
}
.work {
  font-family: $heading;
  font-weight: 900;
  font-size: scale('h2');

  color: $neutral-900;
}

.title__contact {
  display: flex;
  flex-flow: row wrap;
  justify-content: flex-start;
  align-items: center;
  gap: 1.25rem;

  width: 100%;

  @include screen('large') {
    padding: $spacing-lg 0;
  }
}

.image {
  position: relative;
  z-index: -1;

  width: auto;
  height: 25rem;
  // max-height: inherit;

  img {
    width: 100%;
    height: 100%;

    object-fit: contain;
  }

  @include screen(medium) {
    height: 35rem;
  }
  @include screen('large') {
    position: relative;

    height: rem(600);
  }
}
</style>
