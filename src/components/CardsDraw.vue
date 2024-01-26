<template>
  <v-container>
    <v-row justify="center">
      <ThemeToggle />
      <v-col cols="15" md="8" lg="6">
        <v-card class="mx-auto my-15" color="surface" hover>
          <v-row>
            <v-col cols="3">
              <v-avatar size="100">
                <v-img src="https://www.svgviewer.dev/static-svgs/407200/avatar.svg"></v-img>
              </v-avatar>
            </v-col>
            <v-col cols="15">
              <v-card-title class="text--primary">Jean A. Silva</v-card-title>
              <v-card-subtitle class="text--secondary">Developer Full Stack</v-card-subtitle>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts" setup>
import ThemeToggle from '@/components/ThemeToggle.vue'
</script>
