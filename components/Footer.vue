<template>
  <footer>
    <div class="content">
      <footer-menu class="menu" />

      <div class="copyright">
        <logo-link />
        <p>
          Copyright&nbsp;&copy;&nbsp;{{
            new Date().getFullYear()
          }}&nbsp;Elizabeth Nthena. All Rights Reserved.
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
import FooterMenu from './FooterMenu.vue'
import LogoLink from './PageNavigation/LogoLink.vue'
export default {
  name: 'MainFooter',
  components: { LogoLink, FooterMenu },
}
</script>

<style lang="scss" scoped>
footer {
  background-color: $neutral-900;
}

.content {
  padding: 0;
  @include screen(large) {
    @include content-grid;
    padding: $spacing-lg 0;

    .menu,
    .copyright {
      grid-row: 1 / -1;
    }

    .copyright {
      grid-column: 1 / 5;
      align-self: start;
    }
    .menu {
      grid-column: 6 / -2;
    }
  }

  @include screen(x-large) {
    .copyright {
      grid-column: 2 / 6;
      align-self: start;
    }
    .menu {
      grid-column: 7 / -2;
    }
  }
}

.copyright {
  @include flex-wrap-col;
  gap: $spacing-sm;

  color: $neutral-50;
  padding: $spacing-lg 0;

  @include screen(large) {
    padding: 0;
  }
}
</style>
