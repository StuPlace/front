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
      { src: 'https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js' },
      { type: 'text/javascript', src: '/js/bootstrap-navbar.js'},
      { type: 'text/javascript', src:'/js/theme.js'}
    ]
  },
}
</script>

<style>

</style>
