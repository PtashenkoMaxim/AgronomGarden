<script setup>
import Visitors from '/work/AgronomGarden-1/src/components/Visitors.vue'
</script>
<template>
  <img class="TeableHead" src="/HeaderTable.svg" />
  <div class="TableBody">
    <Visitors />
  </div>
</template>
<style scoped>
.TableBody {
  display: flex;
}
.TeableHead {
  width: 100%;
  padding-top: 20px;
}
</style>
