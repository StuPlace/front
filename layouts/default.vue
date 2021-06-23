<template>
  <div>
    <Navbar />
    <Nuxt />
  </div>
</template>

<script>
export default {
  head:{
    title:'Home Page',
    script: [
      { src: 'https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js' },
      { type: 'text/javascript', src: 'js/bootstrap-navbar.js'},
      { type: 'text/javascript', src:'js/theme.js'}
    ]
  },
}
</script>
<style></style>
