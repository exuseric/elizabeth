<template>
  <ul class="menu">
    <li v-for="link in links" :key="link.ref">
      <nuxt-link
        :to="link.ref"
        class="link"
        :aria-disabled="link.disabled"
        :disabled="link.disabled"
      >
        {{ link.name }}
      </nuxt-link>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'PageMenu',
  data() {
    return {
      links: [
        { name: 'home', ref: '/', disabled: false },
        { name: 'services', ref: '/services', disabled: true },
        { name: 'about', ref: '/about', disabled: false },
        { name: 'contact', ref: '/contact', disabled: true },
        { name: 'gallery', ref: '/gallery', disabled: true },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.menu {
  list-style: none;
  padding: 0;

  li {
    margin: $spacing-sm 0;
    padding: 0 $spacing-md;

    a {
      display: block;

      font-size: scale('h2');
      font-family: $body;
      font-weight: 100;

      text-align: left;
      text-transform: capitalize;

      padding: $spacing-md $spacing-sm;
    }
  }

  @include screen(medium) {
    display: flex;
    flex-flow: row wrap;
    justify-content: flex-start;

    li {
      margin: 0;
      padding: 0 $spacing-sm;

      a {
        font-size: scale('base');
        font-weight: 400;
        padding: $spacing-sm;
      }
    }
  }
}

.nuxt-link-exact-active {
  position: relative;
  color: $primary-500;
  font-weight: 600;
}
</style>
