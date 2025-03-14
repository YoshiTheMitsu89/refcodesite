<template>
  <v-container>
    <v-row justify="center" align="center">
      <v-col cols="12" sm="8" md="6">
        <v-card>
          <v-card-title class="text-h4 text-center"> Willkommen bei RefCode </v-card-title>
          <v-card-text class="text-center">
            <p class="text-body-1 mb-6">
              Teilen Sie Ihre Code-Referenzen oder suchen Sie nach vorhandenen Links.
            </p>
            <v-btn color="primary" class="mr-4" prepend-icon="mdi-share" @click="shareLink">
              Link teilen
            </v-btn>
            <v-btn color="secondary" prepend-icon="mdi-magnify" @click="searchLink">
              Link suchen
            </v-btn>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  console.log('HomeView mounted')
})

const shareLink = () => {
  console.log('Share link clicked')
}

const searchLink = () => {
  console.log('Search link clicked')
}
</script>
