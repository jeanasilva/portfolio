<template>
  <div class="d-flex justify-center align-right" style="height: 1vh;">
    <v-btn
      icon
      small
      @click="toggleTheme"
      class="elevation-10"
      :color="buttonColor"
    >
      <v-icon size="40">
        {{ theme.global.name.value === 'light' ? 'mdi-moon-waning-crescent' : 'mdi-white-balance-sunny' }}
      </v-icon>
    </v-btn>
  </div>
</template>

<script lang="ts" setup>
import { computed } from 'vue';
import { useTheme } from 'vuetify';

const theme = useTheme();

const buttonColor = computed(() => theme.global.name.value === 'light' ? 'dark' : 'light');

function toggleTheme() {
  theme.global.name.value = theme.global.name.value === 'light' ? 'dark' : 'light';
}
</script>

<style>
</style>
