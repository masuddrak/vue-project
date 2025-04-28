<script setup>
import { House } from 'lucide-vue-next';


defineProps({
  name: String,
  path: String,
});
</script>

<template>
  <div class="flex items-center gap-1 ">
    <House class="h-[15px]"></House> 
    <a :href="`/${path}`">{{ name }}</a>
  </div>
</template>
