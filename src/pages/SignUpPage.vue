<template>
  <q-page class="flex flex-center" padding>
    <div class="full-width" style="max-width: 400px;">
      <h5 class="q-my-md text-center">
        Sign Up Form
      </h5>

      <q-card class="q-pa-md">

        <q-card-section>

          <q-form>
            <q-input label="Full Name" placeholder="Full Name" filled class="q-mb-md q-mt-md">
              <template v-slot:prepend>
                <q-icon name="mdi-account" />
              </template>
            </q-input>

            <q-input label="Email" placeholder="email@example.com" filled class="q-mb-md">
              <template v-slot:prepend>
                <q-icon name="mdi-email" />
              </template>
            </q-input>

            <q-input label="Password" type="password" filled class="q-mb-md">
              <template v-slot:prepend>
                <q-icon name="mdi-lock" />
              </template>
            </q-input>


            <q-input label="Verify Password" type="password" filled class="q-mb-md">
              <template v-slot:prepend>
                <q-icon name="mdi-lock" />
              </template>
            </q-input>

            <q-btn label="already have an account?" flat to="/login" filled class="q-mb-md" />

            <div class="row" filled>

              <q-btn label="signup" class="full-width" color="positive" />

            </div>

          </q-form>

        </q-card-section>

      </q-card>

      <q-btn class="flex-center" flat color="dark" label="Go To Login Form" to="/login" />

    </div>

  </q-page>
</template>

<script setup>
// async function sendVerifyEmailNotification(email) {
//   try {
//     const response = await fetch('')
//   }
// }
</script>
