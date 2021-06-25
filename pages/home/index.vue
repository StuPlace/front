<template>
<div class="pt-5">
    <div class="row pb-2">
        <div class="col-md-10 text-left">
            <h5 class="d-none d-md-block">Semesters</h5>
        </div>
        <div class="col-md-2">
            <button type="button" class="btn btn-danger rounded-pill order-0" data-bs-toggle="modal" data-bs-target="#exampleModal">
                Create Semester
            </button>
        </div>
    </div>
    <hr>
  <div class="row">
      <div v-for="i in 25" :key="i" class="col-lg-4 col-md-4 pb-4 px-4">
        <Card :card="card" background_image="true" />
      </div>
    </div>
    

    <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <SemesterForm creating="true"/>
    </div>

    
  </div>
</template>

<script>
import SemesterForm from '../../components/SemesterForm.vue'
export default {
  components: { SemesterForm },
    layout:'auth',
    data:() => {
        return {
            card:{
                id: Math.floor(Math.random() * 100),
                title:"hello wosdrld!!!",
                background: 'https://source.unsplash.com/random/200x200?sig='
            },
            background_image: true,
        }
    }
}
</script>

<style>

</style>