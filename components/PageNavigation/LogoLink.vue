<template>
  <nuxt-link to="/" class="logo-link">
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
  align-items: flex-flex-end;
  justify-content: flex-flex-end;

  color: $neutral-900;

  width: fit-content;
  height: fit-content;

  overflow: hidden;

  text-transform: capitalize;
  text-decoration: none;

  .txt {
    font-size: $body;

    align-self: center;
  }
}

.logo-link img {
  width: $icon-btn;
  height: calc($icon-btn / 1.5);

  object-fit: contain;
  object-position: center;
}

.logo-link:hover,
.logo-link:focus-visible {
  color: $primary-50;
  background-color: $primary-500;
  outline-color: $primary-900;
}
</style>
