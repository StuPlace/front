<template>
  <nav class="navbar navbar-expand-lg navbar-light fixed-top py-3" data-navbar-on-scroll="data-navbar-on-scroll">
    <div class="container">
        <NuxtLink class="navbar-brand" to="/">
            <img src="https://i.ibb.co/k64kGBh/image-removebg-preview.png" alt="" width="40" />
            <span class="text-1000 fs-1 ms-2 fw-medium">Stu<span class="fw-bold">Place</span></span>
        </NuxtLink>
      <button class="navbar-toggler collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mx-auto border-bottom border-lg-bottom-0 pt-2 pt-lg-0">
          <li class="nav-item">
            <NuxtLink class="nav-link active active" aria-current="page" to="/" style="display:none">Home</NuxtLink>
          </li>
          <!-- <li class="nav-item">
            <NuxtLink class="nav-link" to="#features">Features</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link" to="#pricing">Pricing </NuxtLink>
          </li> -->
        </ul>
        <div class="d-flex py-3 py-lg-0">
            
          <NuxtLink class="btn btn-link text-1000 fw-medium order-1 order-lg-0" type="button" to="/login">Sign in</NuxtLink>
          <NuxtLink class="btn btn-outline-danger rounded-pill order-0" type="submit" to="/register">Sign Up</NuxtLink>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
}
</script>

<style>

</style>