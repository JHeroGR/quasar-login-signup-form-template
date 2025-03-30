<template>
  <q-page class="flex flex-center" padding>
    <div class="full-width" style="max-width: 400px;">
      <h5 class="q-my-md text-center">
        Sign Up Form
      </h5>

      <q-card>

        <q-card-section>

          <q-form>
            <q-input label="First Name" placeholder="First Name" filled class="q-mb-md" />

            <q-input label="Last Name" placeholder="First Name" filled class="q-mb-md" />

            <q-input label="Email" placeholder="email@example.com" filled class="q-mb-md" />

            <q-input label="Password" type="password" filled class="q-mb-md"/>

            <q-input label="Verify Password" type="password" filled />

          </q-form>

        </q-card-section>

        <q-btn label="signup" class="full-width" color="positive" />


      </q-card>

      <q-btn class="flex-center" flat color="dark" label="Go To Login Form" to="/login" />

    </div>

  </q-page>
</template>

<script setup>
//
</script>
