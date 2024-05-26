<template>
  <Card class="w-[70%] bg-background shadow-lg rounded-lg p-4">
    <!-- Card Header -->
    <CardHeader>
      <CardTitle class="text-lg font-semibold">{{ title }}</CardTitle>
      <CardDescription class="text-base">{{ description }}</CardDescription>
    </CardHeader>
    <!-- Card Content -->
    <CardContent>
      <form @submit.prevent="submitForm" class="flex flex-col space-y-4">
        <div class="flex flex-col space-y-1">
          <Label for="subscriptionType" class="text-sm font-semibold">Subscription Type</Label>
          <Select v-model="subscriptionType" id="subscriptionType" class="px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-500">
            <SelectItem value="sms">SMS</SelectItem>
            <SelectItem value="email">E-Mail</SelectItem>
          </Select>
        </div>
        <div v-if="subscriptionType === 'sms'" class="flex flex-col space-y-1">
          <Label for="sms" class="text-sm font-semibold">Phone Number</Label>
          <Input v-model="contactInfo" id="sms" type="tel" placeholder="Phone Number" class="px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-500" required />
        </div>
        <div v-else class="flex flex-col space-y-1">
          <Label for="email" class="text-sm font-semibold">Email Address</Label>
          <Input v-model="contactInfo" id="email" type="email" placeholder="Email Address" class="px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-500" required />
        </div>
        <div class="flex flex-col space-y-1">
          <Label for="name" class="text-sm font-semibold">Name</Label>
          <Input v-model="name" id="name" type="text" placeholder="Name" class="px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-500" required />
        </div>
        <Button type="submit" class="mt-4 font-semibold py-2 px-4 rounded-lg focus:outline-none focus:shadow-outline">Subscribe</Button>
      </form>
    </CardContent>
  </Card>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const title = 'Subscribe';
const description = 'Select subscription type and enter your contact info';

const name = ref('');
const contactInfo = ref('');
const subscriptionType = ref('email');

const submitForm = () => {
  console.log('Form submitted:', { name: name.value, contactInfo: contactInfo.value, subscriptionType: subscriptionType.value });
};
</script>
