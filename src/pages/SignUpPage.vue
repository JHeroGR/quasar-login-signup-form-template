<template>
  <q-page class="flex flex-center" padding>
    <div class="full-width" style="max-width: 400px;">
      <h5 class="q-my-md text-center">
        Sign Up Form
      </h5>

      <q-card class="q-pa-md">

        <q-card-section>

          <q-form>
            <q-input v-model="name" label="Full Name" placeholder="Full Name" filled class="q-mb-md q-mt-md" :rules="[rules, isEmptyName]">
              <template v-slot:prepend>
                <q-icon name="mdi-account" />
              </template>
            </q-input>

            <q-input v-model="email" label="Email" placeholder="email@example.com" filled class="q-mt-mx" :rules="[rules, isEmailValid]">
              <template v-slot:prepend>
                <q-icon name="mdi-email" />
              </template>
            </q-input>

            <q-input v-model="password" label="Password" type="password" filled class="q-mt-mx" :rules="[required, isPasswordValid]">
              <template v-slot:prepend>
                <q-icon name="mdi-lock" />
              </template>
            </q-input>


            <q-input label="Verify Password" type="password" filled class="q-mt-mx">
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

    </div>

  </q-page>
</template>

<script setup>
import { ref } from 'vue'
import isEmail from 'validator/lib/isEmail'
import isStrongPassword from 'validator/lib/isStrongPassword'
import isEmpty from 'validator/lib/isEmpty'

const name = ref('')
const email = ref('')
const password = ref('')

const required = val => !!val || "This field is required"
const isEmailValid = val => isEmail(val) || "Invalid email format"
const isPasswordValid = val => isStrongPassword(val, { minLowercase: 1, minUppercase: 1, minNumbers: 1, minSymbols: 1}) || "Password must be strong (e.g., 8+ chars, 1 uppercase, 1 lowercase, 1 number, 1 symbol)"
const isEmptyName = val => isEmpty(val) || "Name cannot be blank!"

</script>
