<script setup >
import { AlignJustify } from "lucide-vue-next";
import Slider from "../Slider.vue";
import LeftSide from "./LeftSide.vue";
import RightSide from "./RightSide.vue";
import { ref, onMounted, onUnmounted } from 'vue'


const toggle = ref(false)
const isMdScreen = ref(false)

const checkScreen = () => {
  isMdScreen.value = window.innerWidth >= 768 
}

onMounted(() => {
  checkScreen()
  window.addEventListener('resize', checkScreen)
})

onUnmounted(() => {
  window.removeEventListener('resize', checkScreen)
})
</script>

<template>
  <main class="">
    <div>
      <button
        @click="toggle = !toggle"
        :disabled="isMdScreen"
      >
        <AlignJustify />
      </button>    </div>
    <div class="md:grid md:grid-cols-10 gap-6 relative">
      <div :class="`col-span-2 ${toggle ? 'absolute top-0 w-full h-[50vh] z-[999] flex md:static md:col-span-2 md:flex' : 'hidden md:flex md:col-span-2'}`">

        <LeftSide></LeftSide>
      </div>
      <div class="col-span-6 mb-4 md:mb-0">
        <Slider></Slider>
      </div>
      <div class="col-span-2">
        <div class="flex flex-col gap-4">
          <RightSide></RightSide>
          <RightSide></RightSide>
        </div>
      </div>
    </div>
  </main>
</template>
