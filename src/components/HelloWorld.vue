<template>
  <v-app-bar :elevation="2">
    <template v-slot:prepend>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
    </template>

    <v-app-bar-title>筋トレメモ</v-app-bar-title>
  </v-app-bar>
  <v-sheet
    class="d-flex align-center justify-center flex-wrap text-center mx-auto px-4"
    elevation="4"
    height="250"
    rounded
    max-width="800"
    width="100%"
  >
    <div>
      <h2 class="text-h4 font-weight-black text-orange">今日のトレーニング!</h2>

      <div class="text-h5 font-weight-medium mb-2">
        ここにトレーニング内容を記載！！
      </div>
      <!-- 下記は配列で受け取ってmapで回す -->
      <p class="text-body-2 mb-4">胸トレ:50回</p>
      <p class="text-body-2 mb-4">肩トレ:50回</p>
    </div>
  </v-sheet>
  <TrainingCount />
</template>

<script setup lang="ts">
//
</script>

<style></style>
