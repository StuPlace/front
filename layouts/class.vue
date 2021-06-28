<template>
<div>
    <Navbar />
    <div class="container">
        <section>
            <div class="row">
                <div class="col-3">
                    <Sidebar />
                </div>
                <div class="col-9">
                    <Nuxt />
                </div>
            </div>
        </section>
    </div>
     <Footer />
</div>
</template>

<script>
export default {
  head:{
    title:'Class',
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
