<script setup lang="ts">
let chest_training: Array<string>;
let arm_training: Array<string>;
let shoulder_training: Array<string>;
let back_training: Array<string>;
let foot_training: Array<string>;

chest_training = [
  "ダンベルフライ",
  "ダンベルプレス",
  "ベンチプレス",
  "ケーブルプレス",
];
arm_training = [
  "イージーバーカール",
  "インクラインカール",
  "バイセプスカール",
  "プッシュダウン",
  "ダンベルカール",
];
shoulder_training = [
  "ダンベルフライ",
  "ダンベルプレス",
  "ベンチプレス",
  "ケーブルプレス",
];
back_training = [
  "ダンベルフライ",
  "ダンベルプレス",
  "ベンチプレス",
  "ケーブルプレス",
];
foot_training = [
  "ダンベルフライ",
  "ダンベルプレス",
  "ベンチプレス",
  "ケーブルプレス",
];
let chest_numbers: number;
let chest_weight: number;
let arm_numbers: number;
let arm_weight: number;
let shoulder_numbers: number;
let shoulder_weight: number;
let back_numbers: number;
let back_weight: number;
let foot_numbers: number;
let foot_weight: number;
const emit = defineEmits(["emitTraining", "chestTraining"]);

const addCheastTraining = () => {
  emit("chestTraining", chest_training, chest_numbers, chest_weight);
};

const addArmTraining = () => {
  emit("emitTraining", arm_training, arm_numbers, arm_weight);
};

const addShoulderTraining = () => {
  emit("emitTraining", shoulder_training, shoulder_numbers, shoulder_weight);
};

const addBackTraining = () => {
  emit("emitTraining", back_training, back_numbers, back_weight);
};

const addFootTraining = () => {
  emit("emitTraining", foot_training, foot_numbers, foot_weight);
};
</script>

<template>
  <div class="traning-count">
    <div class="muscle-part">
      <div>胸トレ</div>
      <v-select
        clearable
        label="Select"
        :items="chest_training"
        multiple
      ></v-select>
      <input
        v-model="chest_numbers"
        class="box"
        type="number"
        placeholder="回数"
      />
      <input
        v-model="chest_weight"
        class="box2"
        type="number"
        placeholder="重量"
      />
      <button @click="addCheastTraining" testfn>追加</button>
    </div>

    <div>
      <div class="muscle-part">
        <div>腕トレ</div>
        <v-select
          clearable
          label="Select"
          :items="arm_training"
          multiple
        ></v-select>
        <input
          v-model="arm_numbers"
          class="box"
          type="number"
          placeholder="回数"
        />
        <input
          v-model="arm_weight"
          class="box2"
          type="number"
          placeholder="重量"
        />
        <button @click="addArmTraining" testfn>追加</button>
      </div>
    </div>
    <div>
      <div class="muscle-part">
        <div>肩トレ</div>
        <v-select
          clearable
          label="Select"
          :items="shoulder_training"
          multiple
        ></v-select>
        <input
          v-model="shoulder_numbers"
          class="box"
          type="number"
          placeholder="回数"
        />
        <input
          v-model="shoulder_weight"
          class="box2"
          type="number"
          placeholder="重量"
        />
        <button @click="addShoulderTraining" testfn>追加</button>
      </div>
    </div>
    <div>
      <div class="muscle-part">
        <div>背中トレ</div>
        <v-select
          clearable
          label="Select"
          :items="back_training"
          multiple
        ></v-select>
        <input
          v-model="back_numbers"
          class="box"
          type="number"
          placeholder="回数"
        />
        <input
          v-model="back_weight"
          class="box2"
          type="number"
          placeholder="重量"
        />
        <button @click="addBackTraining" testfn>追加</button>
      </div>
    </div>
    <div>
      <div class="muscle-part">
        <div>脚トレ</div>
        <v-select
          clearable
          label="Select"
          :items="foot_training"
          multiple
        ></v-select>
        <input
          v-model="foot_numbers"
          class="box"
          type="number"
          placeholder="回数"
        />
        <input
          v-model="foot_weight"
          class="box2"
          type="number"
          placeholder="重量"
        />
        <button @click="addFootTraining" testfn>追加</button>
      </div>
    </div>
  </div>
</template>
<style>
.traning-count {
  margin: 10%;
}

.muscle-part {
  margin-bottom: 30px;
}

.v-select {
  margin-right: 10%;
}
.box {
  outline: 2px solid black;
}
.box2 {
  outline: 2px solid black;
  margin-left: 5%;
}
</style>
