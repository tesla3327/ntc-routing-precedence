<template>
  <div>
    <p>
      Adding the <code>keepalive</code> attribute to the
      <code>NuxtPage</code> component will keep the child
      pages alive when navigating between them.
    </p>
    <p>
      You can also add <code>keepalive: true</code> to your
      <code>definePageMeta</code>.
    </p>
    <pre><NuxtPage keepalive /></pre>
  </div>
</template>

<script setup>
// Switch this to true so the children components are kept alive
definePageMeta({
  keepalive: true,
});
</script>
