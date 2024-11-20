<template>
    <div class="flex flex-col gap-2 justify-center items-center bg-gray-50 rounded p-6">
        <h2 class="font-[Inter] text-gray-700 font-regular">
            Entre com a sua conta
        </h2>
        <Button
            @click="emit('wants-login-with-github')"
            :loading="props.loading"
            label="Continuar com o GitHub"
            icon="pi-pi-github"
            icon-pos="right"
        />
    </div>
</template>

<script setup lang="ts">
    const emit = defineEmits<{
        (e: 'wants-login-with-github'): void
    }>()

    const props = defineProps<{
        loading: boolean
    }>()
</script>