<template>
  <v-app>
    <v-main>
      <v-container>
        <v-menu>
          <template v-slot:activator="{ props }">
            <v-btn
              color="primary"
              v-bind="props"
            >
              Activator slot
            </v-btn>
          </template>
          <v-list>
            <v-list-item
              v-for="(item, index) in items"
              :key="index"
              :value="index"
            >
              <v-list-item-title>{{ item }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup lang="ts">
  import { ref } from 'vue';

  const items = ref(["a", "b", "c"]);
</script>
