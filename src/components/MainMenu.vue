<script setup lang="ts">
import { ref } from "vue";

let change_chest_training = ref();
let change_chest_numbers = ref();
let change_chest_weight = ref();

let change_arm_training = ref();
let change_arm_numbers = ref();
let change_arm_weight = ref();

let change_shoulder_training = ref();
let change_shoulder_numbers = ref();
let change_shoulderweight = ref();

let change_back_training = ref();
let change_back_numbers = ref();
let change_back_weight = ref();

let change_foot_training = ref();
let change_foot_numbers = ref();
let change_foot_weight = ref();

const addCheastTraining = (
  chest_training: Array<string>,
  chest_numbers: number,
  chest_weight: number
) => {
  change_chest_training.value = chest_training;
  change_chest_numbers.value = chest_numbers;
  change_chest_weight.value = chest_weight;
};
const addArmTraining = (
  chest_training: Array<string>,
  numbers: number,
  weight: number
) => {
  change_arm_training.value = chest_training;
  change_arm_numbers.value = numbers;
  change_arm_weight.value = weight;
};
const addShoulderTraining = (
  chest_training: Array<string>,
  numbers: number,
  weight: number
) => {
  change_shoulder_training.value = chest_training;
  change_shoulder_numbers.value = numbers;
  change_shoulderweight.value = weight;
};
const addBackTraining = (
  chest_training: Array<string>,
  numbers: number,
  weight: number
) => {
  change_back_training.value = chest_training;
  change_back_numbers.value = numbers;
  change_back_weight.value = weight;
};
const addFootTraining = (
  chest_training: Array<string>,
  numbers: number,
  weight: number
) => {
  change_foot_training.value = chest_training;
  change_foot_numbers.value = numbers;
  change_foot_weight.value = weight;
};
</script>

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

      <!-- 下記は配列で受け取ってmapで回す -->
      <p class="text-body-2 mb-4">
        <div>胸トレ</div>
        {{ change_chest_training }} {{ change_chest_numbers }}{{ change_chest_weight }}
      </p>
    </div>
  </v-sheet>
  <TrainingCount
  @chestTraining="addCheastTraining"
    @emitTraining="
        addArmTraining,
        addShoulderTraining,
        addBackTraining,
        addFootTraining
    "
  />
</template>
<style></style>
