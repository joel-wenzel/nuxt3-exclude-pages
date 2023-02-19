<template>
  <div>
    All routes
    <ul>
      <li v-for="route in routes" :key="route">
        <NuxtLink :to="route">{{ route }}</NuxtLink>
      </li>
    </ul>
  </div>
</template>
<script setup lang="ts">
  const router = useRouter()
  const routes = router.getRoutes().map((r) => r.path)
</script>
