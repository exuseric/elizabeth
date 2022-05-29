<template>
  <nuxt-link to="/" class="logo-link link">
    <img
      src="~/assets/logo/main.png"
      alt="A block abstract of the letter E and N"
      title="logo"
      width="3375"
      height="5396"
    />
    <span class="txt">Elizabeth Nthena</span>
  </nuxt-link>
</template>
<script>
export default {
  name: 'LogoLink',
}
</script>
<style lang="scss" scoped>
.logo-link {
  display: flex;
  flex-flow: row wrap;
  align-items: baseline;
  justify-content: space-between;
  gap: $spacing-md;

  color: $neutral-500;

  width: fit-content;
  height: fit-content;

  padding: $spacing-sm;

  overflow: hidden;

  text-transform: capitalize;
  text-decoration: none;

  .txt {
    font-size: $body;
  }
}

.logo-link img {
  width: $icon-btn * 0.65;
  height: $icon-btn * 0.65;

  object-fit: contain;
  object-position: center;
}

// .logo-link:hover,
// .logo-link:focus-visible {
//   color: $neutral-50;
//   background-color: $neutral-900;
//   outline-color: $primary-900;
// }
</style>
