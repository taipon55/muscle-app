<template>
  <div class="traning-count">
    <div class="muscle-part">
      <div>胸トレ</div>
      <v-select
        clearable
        label="Select"
        :items="[
          'California',
          'Colorado',
          'Florida',
          'Georgia',
          'Texas',
          'Wyoming',
        ]"
        multiple
      ></v-select>
      <input class="box" type="number" placeholder="回数" />

      <div>
        <div class="muscle-part2">
          <div>腕トレ</div>
          <v-select
            clearable
            label="Select"
            :items="[
              'California',
              'Colorado',
              'Florida',
              'Georgia',
              'Texas',
              'Wyoming',
            ]"
            multiple
          ></v-select>
          <input class="box" type="number" placeholder="回数" />
        </div>
      </div>
      <div>
        <div class="muscle-part2">
          <div>肩トレ</div>
          <v-select
            clearable
            label="Select"
            :items="[
              'California',
              'Colorado',
              'Florida',
              'Georgia',
              'Texas',
              'Wyoming',
            ]"
            multiple
          ></v-select>
          <input class="box" type="number" placeholder="回数" />
        </div>
      </div>
      <div>
        <div class="muscle-part2">
          <div>背中トレ</div>
          <v-select
            clearable
            label="Select"
            :items="[
              'California',
              'Colorado',
              'Florida',
              'Georgia',
              'Texas',
              'Wyoming',
            ]"
            multiple
          ></v-select>
          <input class="box" type="number" placeholder="回数" />
        </div>
      </div>
      <div>
        <div class="muscle-part2">
          <div>脚トレ</div>
          <v-select
            clearable
            label="Select"
            :items="[
              'California',
              'Colorado',
              'Florida',
              'Georgia',
              'Texas',
              'Wyoming',
            ]"
            multiple
          ></v-select>
          <input class="box" type="number" placeholder="回数" />
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts"></script>
<style>
.traning-count {
  margin: 10%;
}

.v-select {
  margin-right: 10%;
}
.box {
  outline: 2px solid black;
}
</style>
