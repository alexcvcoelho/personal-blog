<script setup lang="ts">
const route = useRoute()
const { data } = await useAsyncData('get-document', () => queryContent(route.path).findOne())
</script>
<template>
  <div class="main">
    <ContentRenderer :value="data" />
  </div>
</template>