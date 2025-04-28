<script setup lang="ts">
import { AlignJustify } from "lucide-vue-next";
import Slider from "../Slider.vue";
import LeftSide from "./LeftSide.vue";
</script>

<template>
  <main>
    <div>
        <AlignJustify  />
    </div>
    <div class="grid grid-cols-6 gap-4">
      <div>
        <LeftSide></LeftSide>
      </div>
      <div class="col-span-4">
        <Slider></Slider>
      </div>
    </div>
  </main>
</template>
