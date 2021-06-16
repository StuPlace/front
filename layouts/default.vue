<template>
  <div>
    <Navbar />!
    <Nuxt />
  </div>
</template>

<script>
export default {
  head:{
    title:'Home Page',
    script: [
      { src: '/js/bootstrap-navbar.js'},
      {src:'/js/theme.js'}
    ]
  },
}
</script>

<style></style>
