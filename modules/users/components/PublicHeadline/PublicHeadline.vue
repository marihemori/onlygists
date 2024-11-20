<template>
  <div class="w-full flex flex-col justify-center items-center gap-2">
    <div class="w-24 md:w-32 rounded-full overflow-hidden">
      <img class="w-full" :src="props.avatarUrl" alt="User avatar" />
    </div>
    <h1 class="font-[Inter] text-gray-700 text-center font-bold text-2xl md:text-3xl">
      {{ props.name }}
    </h1>
    <p
      v-if="props.bio"
      class="font-[Inter] text-gray-700 text-center font-regular md:text-lg"
    >
      {{ props.bio }}
    </p>
    <p
      v-if="props.city && props.state"
      class="font-[Inter] font-regular text-gray-500 text-sm md:text-base"
    >
      <i class="pi pi-map-marker mr-1"></i>
      {{ props.city }}, {{ props.state }}
    </p>
  </div>
</template>

<script lang="ts" setup>
import { defineProps, withDefaults } from 'vue';

  const props = withDefaults(defineProps<{
     name: string;
     avatarUrl: string;
     bio?: string;
     city?: string;
     state?: string;
  }>(), {
    name: 'Mariana',
    avatarUrl: '',
    bio: 'Front-end developer',
    city: 'São Paulo',
    state: 'SP',
  })
</script>

<style>

</style>