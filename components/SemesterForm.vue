<template>
<div>
  <div class="modal-dialog">
    <div class="modal-content">
        <div class="modal-header">
            <h5 v-if="creating" class="modal-title" id="exampleModalLabel">Create Semester</h5>
            <h5 v-if="edited" class="modal-title" id="exampleModalLabel">Edit {{edited.title}} Semester</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
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
                <label for="supervisor" class="form-label">Supervisor name</label>
                <input type="text" class="form-control" id="supervisor" v-model="form.supervisor">
                  <div class="invalid-feedback">
                    Please enter semster Supervisor.
                  </div>
                </div>
            </div>
            <button v-if="edited" type="submit" class="btn btn-primary">Submit</button>
          </div>
        </div>
        <div class="modal-footer">
            <button v-if="creating" type="button" @click="createSemester(form)" class="btn btn-outline-danger rounded-pill order-0">Create</button>
            <button v-if="edited" type="button" @click="EditSemester(form)" class="btn btn-outline-danger rounded-pill order-0">Edit</button>
        </div>
    </div>
  </div>
</div>

  
</template>

<script>
export default {
    props:['edited','creating'],
    data: () => {
      return {
          form: {
            title: '',
            code: '',
            supervisor: ''
          }
      }
    },
    methods: {
      createSemester: (data) => {
        console.log(data); // do creation here.
      },
      EditSemester: (data) => {
        console.log(data); // do creation here.
      }
    }
}
</script>

<style></style>