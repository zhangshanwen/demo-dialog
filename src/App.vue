<template>
  <v-app>
    <v-navigation-drawer
      image="https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg"
      theme="dark"
      permanent
    >
      <template v-slot:prepend>
        <div class="pa-2">
          <v-btn block>
            Show Dialog1
          </v-btn>
        </div>
      </template>
      <v-list nav>
        <v-list-item v-for="i in 9">
          <div class="pa-2">
            <v-btn> Show Dialog List{{ i }}</v-btn>
          </div>
        </v-list-item>

      </v-list>
      <template v-slot:append>
        <div class="pa-2">
          <v-btn block>
            Show Dialog2
          </v-btn>
        </div>
      </template>

    </v-navigation-drawer>
    <v-main>
      <v-app-bar location="top">
        <v-spacer></v-spacer>
        <v-btn color="primary" > Show Dialog top</v-btn>
        <v-spacer></v-spacer>
      </v-app-bar>
      <v-app-bar location="bottom">
        <v-spacer></v-spacer>
        <v-btn color="primary" > Show Dialog bottom</v-btn>
        <v-spacer></v-spacer>
      </v-app-bar>
      <v-card class="h-100">
        <iframe src="/iframe.html" class="w-100 h-100"></iframe>
      </v-card>
    </v-main>
    <local-dialog v-model="dialog"></local-dialog>
  </v-app>
</template>

<script setup lang="ts">
import LocalDialog from "@/components/LocalDialog.vue";
import {ref} from "vue"

const dialog = ref(false)
</script>

<style></style>
