<template>
<div class="pt-5">
  <div class="row">
      <div v-for="i in 25" :key="i" class="col-lg-4 col-md-4 pb-4 px-4">
        <Card :card="card" background_image="true" />
      </div>
      
  </div>
  </div>
</template>

<script>
export default {
    layout:'auth',
    data:() => {
        return {
            card:{
                title:"hello wosdrld!!!",
                background: 'https://source.unsplash.com/random/200x200?sig='
            },
            background_image: true
        }
    }
}
</script>

<style>

</style>