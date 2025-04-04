<template>

  <q-page class="flex flex-center" padding>
    <div class="full-width" style="max-width: 400px;">
      <h5 class="q-my-md text-center">
        Login Form
      </h5>

      <q-card class="q-pa-md">

        <q-card-section>

          <q-form>

            <q-input label="Email" placeholder="email@example.com" filled class="q-mb-md">
              <template v-slot:prepend>
                <q-icon name="mdi-email" />
              </template>
            </q-input>

            <q-input label="Password" placeholder="password" filled class="q-mb-md">
              <template v-slot:prepend>
                <q-icon name="mdi-lock" />
              </template>
            </q-input>

            <q-checkbox label="Remember Me" :model-value="true" class="q-mb-md"/>

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
