<template>
  <section class="pb-6">
      <div class="container">
        <div class="row flex-center">
          <div class="col-lg-6 col-md-5 order-md-1">
            <img
              class="img-fluid"
              src="~assets/img/illustrations/1.png"
              alt=""
            />
          </div>
          <div class="col-md-7 col-lg-6 mt-5 text-center text-md-start">
            <h1 class="fw-medium">
              Would you like to <br />Orgnize your
              <span class="fw-bold">Academic life?</span>
            </h1>
            <p class="mt-3 mb-4">
              We are providing the most customizable solution for
              <span class="fw-medium">Students. </span>
            </p>
            <!-- If user NOT logged in -->
            <div v-if="true">
              <NuxtLink class="btn btn-lg btn-danger hover-top btn-glow" to="/register"
                >Get Started
              </NuxtLink>
            </div>
            <div v-else>
              <NuxtLink class="btn btn-lg btn-danger hover-top btn-glow" to="/register"
                >Semesters
              </NuxtLink>
            </div>
          </div>
        </div>
      </div>
      <!-- end of .container-->
    </section>
</template>

<script>
export default {

}
</script>

<style>

</style>