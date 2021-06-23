<template>
  <div>
    <div class="row">
      <div class="col-8 col-md-8 has-validation">
        <label for="title" class="form-label">Semester Title</label>
        <input type="text" class="form-control" id="title" required v-model="form.title">
          <div class="invalid-feedback">
            Please enter semster title.
          </div>
      </div>
      <div class="col-4 col-md-4 has-validation">
        <label for="code" class="form-label">Semester Code</label>
        <input type="text" class="form-control" id="code" v-model="form.code">
          <div class="invalid-feedback">
            Please enter semster code.
          </div>
      </div>
    </div>

    <div class="row pt-3">
      <div class="col-12 col-md-12 has-validation">
        <label for="title" class="form-label">Supervisor name</label>
        <input type="text" class="form-control" id="title" v-model="form.supervisor">
          <div class="invalid-feedback">
            Please enter semster Supervisor.
          </div>
        </div>
    </div>

    <button v-if="edited" type="submit" class="btn btn-primary">Submit</button>
  </div>
</template>

<script>
export default {
    props:['edited'],
    data: () => {
      return {
          form: {
            title: '',
            code: '',
            supervisor: ''
          }
      }
    }
}
</script>

<style>

</style>