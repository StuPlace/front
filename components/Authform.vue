<template>
  <div>
      <div class="row align-items-center">
        <div class="col-md-4 col-lg-6 text-lg-center"><img class="img-fluid mb-5 mb-md-0" src="~assets/img/illustrations/2.png" alt="" /></div>
        <div class="col-md-8 col-lg-6 text-lg-center">
            <div class="text-md-start text-center">
              <h4>
                <span class="fw-bold">
                  {{register ? 'Sign up' : 'Sign in'}}
                </span>
              </h4>
            </div>
            <div class="form-group">
              <div class="mb-3 form-group">
                <label for="email" class="form-label">Email</label>
                <input type="email" v-model="form.email" name="email" id="email" class="form-control" placeholder="name@example.com">
              </div>
              <div class="mb-3 form-group">
                <label for="password" class="form-label">Password</label>
                <input type="password" v-model="form.password" name="password" class="form-control" placeholder="Password">
              </div>
              <div>
                <button v-if="register" class="btn btn-outline-danger rounded-pill order-0" @click="signup">Sign Up</button>
                <button v-if="login" class="btn btn-outline-danger rounded-pill order-0" @click="signin">Sign In</button>
              </div>
            </div>
        </div>
        <div>

        </div>
      </div>
  </div>
</template>

<script>
export default {
    props:['register','login'],
    data(){
        return {
            form:{
                email:'',
                password: ''
            }
        }
    },
    methods: {
        signup(){
            console.log(this.form);
        },
        signin(){
            console.log(this.form);
        }
    }

}
</script>

<style>

</style>