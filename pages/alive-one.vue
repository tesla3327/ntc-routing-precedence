<template>
  <p>
    Because both <code>alive-one</code> and
    <code>alive-two</code> have set their
    <code>keepalive</code> property to <code>true</code>, we
    can switch between them while still keeping our pages in
    memory.
  </p>
  <pre><Count /></pre>
</template>

<script setup>
definePageMeta({
  keepalive: true,
});
</script>
