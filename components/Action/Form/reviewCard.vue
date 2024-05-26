<template>
  <Card class="h-48 w-64 flex items-center">
    <CardContent>
      <div class="flex items-center">
        <div>
          <p class="text-lg font-semibold p-2">{{ name }}</p>
          <p class="text-sm text-gray-600 p-2">{{ comment }}</p>
          <StarRating :rating="rating" class="p-2"/>
        </div>
      </div>
    </CardContent>
  </Card>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';
import StarRating from "~/components/Action/Form/StarRating.vue";

const props = defineProps({
  rating: {
    type: Number,
    required: true
  },
  comment: {
    type: String,
    required: true
  },
  name: {
    type: String,
    required: true
  }
});
</script>
