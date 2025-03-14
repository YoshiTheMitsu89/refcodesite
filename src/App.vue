<template>
  <v-app>
    <v-app-bar color="primary">
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-app-bar-title>RefCode</v-app-bar-title>
      <v-spacer></v-spacer>
      <v-btn icon="mdi-share"></v-btn>
      <v-btn icon="mdi-magnify"></v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <router-view v-slot="{ Component }">
          <component :is="Component" />
        </router-view>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup>
import { onMounted } from 'vue'
import { useRouter } from 'vue-router'

const router = useRouter()

onMounted(() => {
  console.log('App mounted')
  console.log('Current route:', router.currentRoute.value)
})
</script>

<style>
html {
  overflow-y: auto;
}
</style>
