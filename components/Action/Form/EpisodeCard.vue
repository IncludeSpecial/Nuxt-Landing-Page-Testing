<template>
  <div class="bg-background/90 flex p-8 mt-8 border-b-2 border-b-primary/20">
    <img :src="image" class="max-w-[389px] rounded-lg" :alt="`Episode {episodeNumber} Image`"/>
    <div class="flex flex-col justify-between ml-8">
      <div><p class="bg-primary text-background p-2 rounded-sm inline-block">{{ category }}</p></div>
      <p class="text-blue-500">Episode {{ episodeNumber }}</p>
      <h2 class="text-7xl font-bold mt-2">{{ title }}</h2>
      <p class="text-2xl mt-4">{{ description }}</p>
<!--      <Button class="btn mt-4">View Episode Detail</Button>-->
      <AlertDialog>
        <AlertDialogTrigger as-child>
          <Button variant="outline">
            View Epicode Detaiil
          </Button>
        </AlertDialogTrigger>
        <AlertDialogContent>
          <AlertDialogHeader>
            <AlertDialogTitle>{{ category }}. {{title}}.</AlertDialogTitle>
            <AlertDialogDescription>
             {{description}}
            </AlertDialogDescription>
          </AlertDialogHeader>
          <AlertDialogFooter>
            <AlertDialogCancel>Cancel</AlertDialogCancel>
            <AlertDialogAction>Continue</AlertDialogAction>
          </AlertDialogFooter>
        </AlertDialogContent>
      </AlertDialog>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps<{
  title: string;
  category: string;
  episodeNumber: string;
  description: string;
  image: string;
}>();
</script>

