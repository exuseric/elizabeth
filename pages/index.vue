<template>
  <main class="home">
    <IndexPageHeader />
    <services />
  </main>
</template>

<script>
import Services from '~/components/IndexPage/Services.vue'
export default {
  name: 'HomePage',
  components: { Services },
  layout: 'default',
}
</script>

<style lang="scss" scoped></style>
