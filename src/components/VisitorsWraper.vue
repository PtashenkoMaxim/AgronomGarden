<script setup>
const props = defineProps({
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
      <tr class="TableBody">
        <th>{{ Name }}</th>
        <th>{{ Group }}</th>
        <th>{{ Company }}</th>
        <th>{{ Presence }}</th>
      </tr>
    </div>
  </div>
</template>
<style>
.TableBody {
  display: flex;
  gap: 100px;
}
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
