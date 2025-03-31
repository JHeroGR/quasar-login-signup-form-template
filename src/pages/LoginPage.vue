<template>

  <q-page class="flex flex-center" padding>
    <div class="full-width" style="max-width: 400px;">
      <h5 class="q-my-md text-center">
        Login Form
      </h5>

      <q-card class="q-pa-md" :style="{ backgroundColor: backgroundColor }">

        <q-card-section>

          <q-form>

            <q-input label="Email" placeholder="email@example.com" filled class="q-mb-md" />

            <q-input label="Password" type="password" filled />

            <q-checkbox label="Remember Me" :model-value="true" />

            <div class="row q-gutter-sm">
              <q-btn label="login" class="full-width col-3" color="primary" />

              <q-btn label="forgot password?" class="full-width col-3" color="primary" />
            </div>
          </q-form>

        </q-card-section>
      </q-card>

      <q-btn class="flex-center" flat color="dark" label="Go To SignUp Form" to="/signup" />


    </div>

  </q-page>

</template>

<script>
export default {
  data() {
    return {
      backgroundColor: '#fffff',
    }
  }
}
//
</script>
