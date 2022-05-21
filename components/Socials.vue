<template>
  <ul role="list">
    <li>
      <a
        href="https://www.instagram.com/"
        target="_blank"
        rel="noopener noreferrer"
        aria-disabled="true"
        disabled
        aria-label="Message or connect on Instagram"
      >
        <span class="icon">
          <Instagram aria-hidden="true" focusable="false" />
        </span>
      </a>
    </li>
    <li>
      <a
        href="https://wa.me/+254"
        target="_blank"
        rel="noopener noreferrer"
        aria-disabled="true"
        disabled
        aria-label="Message or call me on WhatsApp"
      >
        <span class="icon">
          <WhatsApp aria-hidden="true" focusable="false" />
        </span>
      </a>
    </li>
    <li>
      <a
        href="te:+254*********"
        target="_blank"
        rel="noopener noreferrer"
        aria-disabled="true"
        disabled
        aria-label="Call me on mobile"
      >
        <span class="icon">
          <MobilePhone aria-hidden="true" focusable="false" />
        </span>
      </a>
    </li>
  </ul>
</template>

<script>
import Instagram from '~/assets/icons/instagram.svg?inline'
import WhatsApp from '~/assets/icons/bxl:whatsapp-square.svg?inline'
import MobilePhone from '~/assets/icons/mobile.svg?inline'
export default {
  name: 'SocialLinks',
  components: {
    Instagram,
    WhatsApp,
    MobilePhone,
  },
}
</script>

<style lang="scss" scoped>
ul {
  @include flex-wrap-row;
  gap: $spacing-sm;

  margin: 0;
  padding: 0;

  width: fit-content;
}
a {
  @include center;
  width: $icon-btn;
  height: $icon-btn;

  text-decoration: none;

  font-size: scale('h5');
  color: $neutral-900;
  background-color: transparent;

  transition: all 0.35s cubic-bezier(0.47, 0, 0.745, 0.715);

  svg {
    width: 100%;
    height: 100%;
  }

  &:hover {
    color: $primary-500;
    border-color: currentColor;
  }
}
</style>
