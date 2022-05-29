<template>
  <ul class="footer-links">
    <li>
      <nuxt-link to="/" class="main-link">Home</nuxt-link>
    </li>
    <!-- About Sub-Menu -->
    <li>
      <nuxt-link to="/about" class="main-link">About</nuxt-link>
      <ul class="sub-menu">
        <li>
          <nuxt-link to="/about#bio">Bio</nuxt-link>
        </li>
      </ul>
    </li>
    <!-- Services Sub-Menu -->
    <li>
      <nuxt-link to="/services" class="main-link">Services</nuxt-link>
      <ul class="sub-menu">
        <li>
          <nuxt-link to="/services#appointment"> Appointment </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/services#location"> Locations </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/services#pricing">Pricing</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/gallery">Gallery</nuxt-link>
        </li>
      </ul>
    </li>
    <!-- Contact Sub-Menu -->
    <li>
      <nuxt-link to="/contact" class="main-link">Contact</nuxt-link>
      <ul class="sub-menu">
        <li>
          <a href="mailto:info@email.com">info@email.com</a>
        </li>
        <li>
          <a href="tel:+254759317671">+254759317671</a>
        </li>
      </ul>
      <Socials class="socials" />
    </li>
  </ul>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
ul {
  margin: 0;
  padding: 0;

  list-style-type: none;

  a {
    text-decoration: none;
  }
}

.footer-links {
  @include flex-wrap-col;
  gap: $spacing-md;

  padding-top: $spacing-lg;

  .main-link {
    font-size: scale('h5');
    font-weight: 600;
    color: $neutral-900;
  }

  .socials {
    color: $neutral-50;
  }

  @include screen(medium) {
    @include flex-wrap-row;
    justify-content: space-between;
  }

  @include screen(large) {
    padding-top: 0;
  }
}

.sub-menu {
  li {
    padding: $spacing-sm * 0.5 0;
  }
  a {
    color: $neutral-500;
  }
}
</style>
