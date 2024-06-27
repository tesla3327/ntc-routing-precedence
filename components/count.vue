<template>
  {{ count }}
</template>

<script setup>
const count = ref(0);
onMounted(() => {
  setInterval(() => count.value++, 1000);
});
</script>
