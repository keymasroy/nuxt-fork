<script setup lang="ts">
definePageMeta({
  middleware: () => {
    if (import.meta.server || useNuxtApp().isHydrating) { return }
    return abortNavigation({
      fatal: true,
    })
  },
})
const router = useRouter()
onNuxtReady(() => router.push({ path: '/middleware-abort', force: true }))
</script>

<template>
  <div>
    <!--  -->
  </div>
</template>
