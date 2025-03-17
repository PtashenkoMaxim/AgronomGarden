<script setup>
import VisitorsList from './VisitorsList.vue'

const Users = [
  {
    Name: 'Max',
    Group: 'Zavod',
    Company: 'Kalash',
    Presence: false,
    Id: 1,
  },
  {
    Name: 'Katya',
    Group: 'Zavod',
    Company: 'IRZ',
    Presence: true,
    Id: 2,
  },
]
function AddVisiter() {
  alert()
}
</script>
<template>
  <div class="VisitorTable">
    <VisitorsList
      :AddVisiter="AddVisiter"
      v-for="User in Users"
      :key="User.Id"
      :Name="User.Name"
      :Group="User.Group"
      :Company="User.Company"
      :Presence="User.Presence"
    />
  </div>
</template>
<style></style>
