<template>
<div>
    <Navbar />
  <section class="pt-4 pt-md-6">
    <div class="container">
        <Nuxt />
    </div>
  </section>
  <Footer />
</div>
</template>

<script>
export default {
  head:{
    title:'Authentication',
    script: [
      { src: '/js/bootstrap-navbar.js' },
      { src:'/js/theme.js' }
    ]
  },
}
</script>

<style>

</style>
