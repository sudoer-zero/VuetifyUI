<template>
  <v-app-bar>
      <img src="@/assets/logo.svg"
        class="flex-shrink-0 ml-6"
        style="width: 40px; height: 40px;" />
       <h2 class="ml-2">Vuetify UI</h2>
      <v-spacer></v-spacer>
      <v-btn text @click="$router.push('/')">Home</v-btn>
      <v-btn @click="toggleTheme" color="primary"> theme </v-btn>
    </v-app-bar>
</template>

<script setup>
import { useTheme } from 'vuetify'

const theme = useTheme()

function toggleTheme() {
  theme.global.name.value = theme.global.current.value.dark ? 'light' : 'dark'
}
</script>

