<template>
  <main class="home">
    <IndexPageHeader />
    <services />
    <contact-form />
  </main>
</template>

<script>
import ContactForm from '~/components/ContactForm.vue'
import Services from '~/components/IndexPage/Services.vue'
export default {
  name: 'HomePage',
  components: { Services, ContactForm },
  layout: 'default',
}
</script>

<style lang="scss" scoped></style>
