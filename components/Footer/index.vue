<template>
  <footer>
    <div class="wrapper">
      <div class="copyright">
        <LogoLink />
        <p>
          Copyright&nbsp;&copy;&nbsp;{{
            new Date().getFullYear()
          }}&nbsp;Elizabeth Nthena. All Rights Reserved.
        </p>
      </div>
      <!-- <footer-menu class="menu" /> -->
      <FooterMenu class="menu" />
    </div>
  </footer>
</template>

<script>
export default {
  name: 'PageFooter',
}
</script>

<style lang="scss" scoped>
footer {
  background-color: $neutral-50;

  @include screen(medium) {
    padding: $spacing-md $spacing-lg;
  }
  @include screen(large) {
    padding: $spacing-md;
  }
}

.wrapper {
  padding: 0;
  @include screen(large) {
    @include grid-flow-col;
    padding: $spacing-lg 0;

    .copyright {
      align-self: start;
    }
    .menu {
      min-width: rem(700);
    }
  }
}

.copyright {
  @include flex-wrap-col;
  gap: $spacing-sm;

  color: $neutral-500;
  padding: $spacing-lg 0;

  @include screen(large) {
    padding: 0;
  }
}
</style>
