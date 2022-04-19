<template>
  <ul role="list">
    <li>
      <a
        href="https://www.instagram.com/"
        target="_blank"
        rel="noopener noreferrer"
        aria-disabled="true"
        disabled
      >
        <span class="text">Connect On Instagram.</span>
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
      >
        <span class="text">Message On WhatsApp</span>
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
      >
        <span class="text">Give Me A Call</span>
        <span class="icon">
          <MobilePhone aria-hidden="true" focusable="false" />
        </span>
      </a>
    </li>
  </ul>
</template>

<script>
import Instagram from '~/assets/icons/instagram.svg?inline'
import WhatsApp from '~/assets/icons/whatsapp.svg?inline'
import MobilePhone from '~/assets/icons/smartphone.svg?inline'
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
  @include flow($gap: $spacing-md, $column-width: $button-width);

  margin: $spacing-md 0;
  padding: 0;
}
a {
  @include grid-flow(
    $flow: column,
    $gap: 0.125rem,
    $justify: space-between,
    $align: center
  );
  font-size: font-size('h6');
  font-weight: 600;

  text-decoration: none;

  width: 100%;
  height: $button-height;

  padding: 0 $spacing-sm;

  color: neutral('black');
  // background-color: secondary('main');
  background: linear-gradient(65deg, primary('light'), secondary('light'));

  border-radius: 0.625rem;
}
</style>
