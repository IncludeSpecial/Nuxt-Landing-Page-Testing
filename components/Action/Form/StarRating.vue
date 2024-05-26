<template>
  <div class="flex items-center space-x-1">
    <template v-for="index in 5">
      <Icon :name="getStarIcon(index)" class=""/>
    </template>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps({
  rating: {
    type: Number,
    required: true
  }
});

const getStarIcon = (index: number): string => {
  return index <= props.rating ? "mdi:star" : "mdi:star-outline";
};
</script>
