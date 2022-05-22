<template>
  <div>
    <PageNavigation />
    <div>
      <Nuxt />
    </div>
    <Footer />
  </div>
</template>

<script>
import Footer from '~/components/Footer.vue'
export default {
  name: 'DefaultLayout',
  components: { Footer },
}
</script>
