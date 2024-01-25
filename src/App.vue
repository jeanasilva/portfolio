<template>
  <v-app>
    <v-app-bar app>
      <!-- Botão de alternância do tema -->
      <v-btn icon @click="toggleTheme">
        <v-icon>
          <!-- Mudar ícone baseado no tema -->
          {{ theme.global.name.value === 'light' ? 'mdi-moon-waning-crescent' : 'mdi-white-balance-sunny' }}
        </v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script lang="ts" setup>
import { useTheme } from 'vuetify';

const theme = useTheme();

function toggleTheme() {
  theme.global.name.value = theme.global.name.value === 'light' ? 'dark' : 'light';
}
</script>
