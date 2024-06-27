<template>
  <div class="prose m-auto max-w-xl py-8">
    <h1>Keepin' those pages alive</h1>
    <p>
      We can prevent Nuxt from destroying our pages by using
      the <code>keepalive</code> property in different ways.
    </p>
    <p>
      Click around on the links below while modifying the
      code to see the different behaviours.
    </p>
    <hr />
    <pre>{{ $route.path }}</pre>
    <div class="grid grid-cols-5 justify-between">
      <NuxtLink v-for="link in nav" :to="link.to">
        {{ link.name }}
      </NuxtLink>
    </div>
    <div
      class="mt-8 px-8 py-4 border rounded-lg bg-slate-50"
    >
      <NuxtPage />
    </div>
  </div>
</template>

<script setup>
const nav = [
  { name: 'Home', to: '/' },
  { name: 'Child', to: '/child' },
  { name: 'Child/One', to: '/child/one' },
  { name: 'Child/Two', to: '/child/two' },
  { name: 'Child/Three', to: '/child/three' },

  { name: 'Alive (one)', to: '/alive-one' },
  { name: 'Alive (two)', to: '/alive-two' },
];
</script>
