<script lang="ts" setup>
import { ref } from "vue";

const value = ref("");
const options = [
  {
    value: "Option1",
    label: "Mts, Men tuxum sotaman. Do'koni",
  },
];
</script>

<template>
  <nav class="w-full bg-stoneGray h-20 shadow-md">
    <div class="container mx-auto flex items-center justify-between h-full px-4">
      <!-- Logo Section -->
      <div class="flex items-center">
        <img class="w-20" src="@/assets/logo.png" alt="Logo" />
        
      </div>

      <!-- Navigation Links -->
      <div class="flex items-center space-x-6">
        <a href="#" class="text-white hover:text-gray-300 transition">Bosh sahifa</a>
        <a href="#" class="text-white hover:text-gray-300 transition">Biz haqimizdagit commit -m "first commit"</a>
        <el-select
          v-model="value"
          placeholder="Select"
          style="width: 240px"
          class="text-black"
        >
          <el-option
            v-for="item in options"
            :key="item.value"
            :label="item.label"
            :value="item.value"
          />
        </el-select>
      </div>

      <!-- Action Buttons -->
      <div class="flex items-center space-x-4">
        <el-button type="primary" class="bg-blue-500 hover:bg-blue-600 text-white">
          Ro'yxatdan o'tish
        </el-button>
        <el-button type="success" class="bg-green-500 hover:bg-green-600 text-white">
          Kirish
        </el-button>
      </div>
    </div>
  </nav>
</template>

<style>
/* Custom styles for the navbar */
nav {
  background-color: #2c3e50; /* Dark gray background */
}
</style>
