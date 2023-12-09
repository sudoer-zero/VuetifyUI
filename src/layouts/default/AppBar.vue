<template>
  <v-container>
    <v-responsive class="align-center text-center">
      <v-row class="d-flex align-center justify-center py-2">
        <v-col cols="auto">
          <v-btn @click="toggleTheme" color="accent">{{ theme.global.current.value.dark ? 'Light' : 'Dark' }}</v-btn>
        </v-col>
      </v-row>
    </v-responsive>
  </v-container>
</template>

<script setup>
import { useTheme } from 'vuetify'

const theme = useTheme()

function toggleTheme() {
  theme.global.name.value = theme.global.current.value.dark ? 'light' : 'dark'
}
</script>

