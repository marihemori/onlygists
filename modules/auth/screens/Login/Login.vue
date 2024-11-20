<template>
  <section class="w-full h-screen flex flex-col items-center justify-center gap-5 bg-gray-50">
    <Logo />
    <SocialForm :loading="loading" @wants-login-with-github="handleGithubLogin" />
  </section>
</template>

<script setup lang="ts">
  import SocialForm from '@/modules/auth/components/SocialForm/SocialForm.vue';

  const loading = ref<boolean>(false);

  const handleGithubLogin = async () => {
    loading.value = true;
    // @TODO: call github api
  }
</script>