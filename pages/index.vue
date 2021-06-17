<template>
  <div>
    <MainHero />
    <MainAccomplish />
    <MainFeatures />
    <Plans />
    <!-- <UsedBy/> -->
    <Reviews />
    <Newsletter />
    <Footer />
  </div>
</template>

<script>
export default {
  data(){
    return {
      title: 'StuPlace | Organize your academic life'
    }
  },
  head(){
    return{
    title: this.title,
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        hid: 'StuPlace is a website that organizes your academic life.',
        name: 'StuPlace is a website that organizes your academic life.',
        content: 'StuPlace is a website that organizes your academic life.'
      }
    ],
  }
  }
}
</script>

<style></style>
