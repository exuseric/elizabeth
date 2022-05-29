<template>
  <div>
    <PageNavigation />
    <div class="nuxt-wrapper">
      <Nuxt />
    </div>
    <div class="nuxt-wrapper">
      <Footer />
    </div>
  </div>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
</script>
<style lang="scss" scoped>
.nuxt-wrapper {
  padding: 0 $spacing-md;
}
</style>
