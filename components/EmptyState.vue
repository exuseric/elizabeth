<template>
  <section class="empty">
    <div class="wrapper content-grid__child">
      <header class="wrapper__header">
        <div class="content">
          <div class="wrapper__header-image">
            <nuxt-img
              fit="contain"
              quality="80"
              format="webp"
              width="400"
              height="400"
              src="/images/header/main-header.png"
              alt="composite of a woman with flowers on a red circle backdrop"
            />
          </div>
          <div class="wrapper__header-heading">
            <h1>ELIZABETH NTHENA</h1>
            <p>Makeup Artist</p>
          </div>
        </div>
      </header>
      <article class="wrapper__social">
        <div class="content">
          <header>
            <h2>Under Construction</h2>
            <p>Don't worry! We can still get in touch.</p>
          </header>

          <Socials class="wrapper__social-links" />
        </div>
      </article>
    </div>
  </section>
</template>

<script>
export default {
  name: 'EmptyState',
}
</script>

<style lang="scss" scoped>
.empty {
  @include content-grid;
  width: 100%;
  background: primary('light');
}

.wrapper {
  // @include grid($grid-count: 6, $gap: 0);
  // @include grid-row($gap: 0, $sizes: repeat(8, 10rem));
  align-self: center;
  // height: 200rem;
  // min-height: 100vh;
  height: fit-content;
  // &__header,
  // &__social {
  //   grid-column: 1 / -1;
  // }

  // &__header {
  //   grid-row: 2 / 5;
  // }

  // &__social {
  //   grid-row: 5 / -1;
  // }
}

.wrapper__header {
  @include center;
  height: 50rem;

  .content {
    // @include grid($grid-count: 6, $gap: 0);
    height: 40rem;

    .wrapper__header-image,
    .wrapper__header-heading {
      grid-column: 1 / -1;
    }

    .wrapper__header-image {
      grid-row: 2 / -1;
    }
    .wrapper__header-heading {
      grid-row: 1 / 4;
    }
  }
}

.wrapper__header-image {
  position: relative;
  z-index: 1;

  min-width: 20rem;
  width: 100%;
  height: auto;

  // border-radius: 20rem;
  overflow: hidden;

  img {
    width: 100%;
    height: 100%;

    object-fit: contain;
    object-position: bottom;
  }

  &::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 2;

    width: inherit;
    height: inherit;

    // background-color: primary('main');
    // mix-blend-mode: hard-light;
    // backdrop-filter: grayscale(1);
  }
}

.wrapper__header-heading {
  z-index: 2;
  text-align: center;
  line-height: 0.5;

  h1 {
    font-size: font-size('display');
    font-family: $heading;
    font-weight: normal;
    line-height: 0.85;

    color: primary('main');
  }

  p {
    font-family: $heading;
    font-size: font-size('h3');
    padding: $spacing-sm 0;

    color: primary('dark');
  }
}

.wrapper__social {
  @include center;

  height: 40rem;
  margin-top: -10rem;
  // padding: 0 $spacing-sm;
  background: primary('main');

  header {
    text-align: center;
    color: primary('light');

    h2 {
      font-size: font-size('h2');
      line-height: 1.125;
    }
  }

  &-links {
    color: primary('light');
  }
}

.catch {
  font-size: font-size('display');
  color: primary('dark');
}
// article:nth-child(1) {
//   // @include mid-screen {
//   //   grid-column: 2 / 7;
//   // }
//   h1 {
//     font-size: font-size('h1');
//     font-family: $heading;
//     font-weight: normal;
//     line-height: 0.85;

//     color: primary('main');
//   }

//   p {
//     font-family: $heading;
//     font-size: font-size('h3');
//     padding: $spacing-sm 0;

//     color: primary('dark');
//   }
// }

// article:nth-child(2) {
//   text-align: center;

//   @include mid-screen {
//     grid-column: 8 / -1;
//   }

//   h2 {
//     font-size: font-size('h3');
//   }
// }
</style>
