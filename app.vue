<template>
  <div class="prose m-auto max-w-xl py-8">
    <h1>Routing Precedence</h1>
    <p>
      A file will always take precedence over a directory
      with the same name. In this example, when we go to the
      route
      <code>/child</code> we match to the file
      <code>/pages/child.vue</code> and <em>not</em> the
      file at <code>/pages/child/index.vue</code>.
    </p>
    <p>
      However, if we get rid of the
      <code>/pages/child.vue</code> component (or rename it
      just to test) we can render these other routes
      directly.
    </p>
    <p>
      The other solution is to add a
      <code>NuxtPage</code> component to
      <code>/pages/child.vue</code> so that we can then
      render the child routes.
    </p>
    <hr />
    <pre>{{ $route.path }}</pre>
    <div class="grid grid-cols-4 justify-between">
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
];
</script>
