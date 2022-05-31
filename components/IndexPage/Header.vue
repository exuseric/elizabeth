<template>
  <header class="hero">
    <div class="wrapper">
      <article class="title">
        <div class="title__heading">
          <h1 class="work">
            Let's express who you are on the inside with limitless possibilities
          </h1>
          <h1 class="name">Elizabeth Nthena &mdash; Makeup Artist</h1>
        </div>
        <div class="title__contact">
          <nuxt-link to="/contact" class="contact__btn primary-btn">
            Hire Me
          </nuxt-link>

          <nuxt-link to="/gallery" class="sec-btn gallery-btn">
            Gallery
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
    </div>
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
  height: 100%;
  padding: 0;
  margin: 0;

  background: $neutral-50;
  // overflow-x: hidden;
}

.wrapper {
  @include content-grid;
  position: relative;
  z-index: 1;

  height: rem(1000);

  .title,
  .image {
    grid-column: 1 / -1;
    align-self: center;
  }

  @include screen(small) {
    // height: fit-content;
    height: rem(500);

    .title {
      grid-column: 1 / 5;
    }

    .image {
      // margin-top: rem(-250);
      grid-column: 5 / -1;
      // width: rem(250);
      width: 100%;
      height: inherit;
    }
  }

  @include screen(medium) {
    height: rem(600);
    padding: $spacing-md 0;

    .title {
      grid-column: 1 / 9;
      grid-row: 1 / -1;
    }
    .image {
      grid-column: 8 / -1;
      grid-row: 1 / -1;
      z-index: -1;
      width: 100%;
      height: inherit;
      margin-top: 0;
    }
  }
  @include screen(large) {
    height: rem(800);
    padding: $spacing-lg 0;

    .title {
      grid-column: 1 / 7;
      grid-row: 1 / -1;
    }
    .image {
      grid-column: 8 / -1;
      grid-row: 1 / -1;
      margin-top: 0;
      width: 100%;
      height: inherit;
    }
  }

  @include screen(x-large) {
    height: rem(700);
  }
}

.image {
  width: auto;

  margin: auto;

  img {
    object-fit: contain;
  }
}

.title {
  align-self: start;
  max-width: rem(800);
  padding: $spacing-lg 0;

  .name {
    font-size: scale('h5');
    font-weight: 400;

    color: $primary-500;

    margin-top: $spacing-md;
    width: fit-content;
  }

  .work {
    font-family: $heading;
    font-weight: 100;
    font-size: scale('h2');

    color: $neutral-900;

    @include screen(x-large) {
      font-size: scale('h1');
    }
  }

  @include screen(large) {
    max-width: 100%;
  }
}

.title__contact {
  @include flex-wrap-row;
  gap: 1.25rem;

  width: 100%;
  padding-top: $spacing-lg;

  @include screen(medium) {
    max-width: rem(400);
  }

  @include screen('large') {
    padding: $spacing-lg 0;
    max-width: 100%;
  }
}
</style>
