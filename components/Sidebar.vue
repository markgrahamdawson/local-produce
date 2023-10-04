<template>
  <div 
    class="fixed min-h-screen w-64 bg-slate-500 top-0 transition-all duration-500"
    :class="sidebarOpen ? 'left-0' : '-left-48'"
    >
    <button @click="sidebarOpen = !sidebarOpen" class="w-full bg-blue-500">
      toggle
    </button>
    <h1>LocalProduce</h1>
  </div>
</template>

<script setup lang="ts">

const sidebarOpen = ref(false)

</script>