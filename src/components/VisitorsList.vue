<script setup>
defineProps({
  AddVisiter: Function,
  Name: String,
  Company: String,
  Group: String,
  Presence: Boolean,
})
</script>
<template>
  <div class="VisitorTable">
    <div class="VisitorBody">
      <h1>{{ Name }}</h1>
      <h1>{{ Group }}</h1>
      <h1>{{ Company }}</h1>
      <h1>{{ Presence }}</h1>
    </div>
  </div>
</template>
<style>
.VisitorBody {
  display: flex;
  align-items: center;
  gap: 20px;
}
.VisitorTable {
  align-items: center;
  flex-direction: column;
}
</style>
