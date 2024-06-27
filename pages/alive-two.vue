<template>
  <p>
    Because both <code>alive-one</code> and
    <code>alive-two</code> have set their
    <code>keepalive</code> property to <code>true</code>, we
    can switch between them while still keeping our pages in
    memory.
  </p>
  <p>
    If you add this property to the <code>child</code> page
    as well, you can navigate between all pages except Home
    without destroying any of the pages.
  </p>
  <pre><Count /></pre>
</template>

<script setup>
definePageMeta({
  keepalive: true,
});
</script>
