<template>
  <div class="card shadow">
       <div v-if="background_image" class="card-img-top cover" :style="`background-image: url('${card.background}${Math.floor(Math.random() * 77)}')`"></div>
        <div class="card-body">
            <div class="row h-50">
                <div class="col-md-12 col-12 col-lg-12">
                    <NuxtLink class="link-primary" to="2">
                        <h3>{{card.title}}</h3>
                    </NuxtLink>
                </div>
                <div class="row mt-3">
                    <div class="col-md-12 col-12 col-lg-12">
                        <NuxtLink class="btn btn-outline-danger rounded-pill order-0" to="2">Continue</NuxtLink>
                    </div>
                </div>
            </div>

        </div>
  </div>
</template>

<script>
export default {
    props: ['background_image','card']
}
</script>

<style scoped>
.shadow {
    box-shadow: 0 .125rem .25rem rgba(0,0,0,.075)!important;
}

.cover {
    height: 180px;
    background-size: cover;
    background-position: center center;
}

.card-img-top {
    width: 100%;
    border-top-left-radius: calc(4px - 1px);
    border-top-right-radius: calc(4px - 1px);
}

.card:hover{
    box-shadow: 0px 0px 19px 4px rgba(0,0,0,.075)!important;
}
</style>