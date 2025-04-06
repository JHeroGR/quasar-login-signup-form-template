<template>
  <q-btn @click="changetheme" class="q-mr-md q-mr-md" :color="$q.dark.isActive ? 'white' : 'dark'" :label="$q.dark.isActive ? 'Light Mode' : 'Dark Mode'" :text-color="$q.dark.isActive ? 'dark' : 'white'" />
</template>

<script setup>
import { watch } from 'vue'
import { useQuasar } from 'quasar'

const $q = useQuasar()

function changetheme() {
  $q.dark.toggle()

}
watch(() => $q.dark.isActive,val => console.log(val ? 'dark': 'light'))
</script>

<style>
  .body--light {
    background-color: white;
    color: black;
  }

  .body--dark {
    background-color: black;
    color: white;
  }
</style>
