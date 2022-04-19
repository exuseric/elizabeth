<template>
  <section class="empty">
    <article class="child">
      <header>
        <div class="image">
          <img
            src="~/assets/images/woman-line.png"
            alt="collage of a female line art with a backdrop of pyramids and lips"
          />
        </div>
        <div class="header-group">
          <h1>ELIZABETH NTHENA</h1>
          <p>Makeup Artist</p>
        </div>
      </header>
    </article>
    <article class="child">
      <h2>Under Construction</h2>
      <p>Don't worry! We can still get in touch.</p>

      <Socials />
    </article>
  </section>
</template>

<script>
export default {
  name: 'EmptyState',
}
</script>

<style lang="scss" scoped>
.empty {
  @include content-grid($column-no: 12);
  width: 100%;
  height: 100vh;

  article {
    grid-column: 1 / -1;
    align-self: center;

    margin: $spacing-md 0;
  }
}

.tagline {
  position: absolute;
  top: 0;
  left: 0;
}

header {
  @include center-grid;
  text-align: center;

  @include mid-screen {
    @include grid($count: 6, $gap: 0);
    align-items: center;

    text-align: left;

    .header-group {
      grid-column: 1 / 4;
      grid-row: 1 / -1;
      justify-self: start;
    }

    .image {
      grid-column: 3 / -1;
      grid-row: 1 / -1;
    }
  }
}

.image {
  width: 25rem;
  height: auto;
}

article:nth-child(1) {
  @include mid-screen {
    grid-column: 2 / 7;
  }
  h1 {
    font-size: font-size('h1');
    font-family: $display;
    font-weight: normal;
    line-height: 1.125;

    color: primary('main');
  }

  p {
    font-family: $heading;
    font-size: font-size('h4');
  }
}

article:nth-child(2) {
  text-align: center;

  @include mid-screen {
    grid-column: 8 / -1;
  }

  h2 {
    font-size: font-size('h3');
  }
}
</style>
