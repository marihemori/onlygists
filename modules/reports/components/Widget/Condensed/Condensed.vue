<template>
  <div class="flex flex-1 flex-col bg-white p-5 rounded-xl">
    <span class="font-[Inter] text-4xl text-primary-500 font-bold">
      {{ props.value }}
    </span>
    <p class="font-[Inter] text-lg text-gray-700">
      {{ props.label }}
    </p>
  </div>
</template>

<script lang="ts" setup>
  const props = defineProps<{
     value: number | string;
     label: string;
  }>()
</script>

<style>

</style>