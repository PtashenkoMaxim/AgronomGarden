<script setup>
import VisitorsWraper from './VisitorsWraper.vue'
import { provide, ref } from 'vue'

const NewVisiter = {
  Name: '',
  Group: '',
  Company: '',
  Presence: false,
  Id: 10,
}

const Name = ref('')
const Group = ref('')
const Company = ref('')
const Presence = ref('')

const AddVisiter = () => {
  NewVisiter.Name = Name.value
  NewVisiter.Group = Group.value
  NewVisiter.Company = Company.value
  NewVisiter.Presence = Presence.value
  const update = { ...NewVisiter }
  console.log(update)
  Users.value.push(update)
}

const Users = ref([
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
])

provide('Users', Users)
</script>
<template>
  <div class="VisitorTable">
    <input placeholder="Имя пользователя" v-model="Name" type="text" />
    <button @click="AddVisiter">добавить Пользователи</button>
    <table>
      <thead>
        <VisitorsWraper
          v-for="User in Users"
          :key="User.Id"
          :Name="User.Name"
          :Group="User.Group"
          :Company="User.Company"
          :Presence="User.Presence"
        />
      </thead>
    </table>
  </div>
</template>
<style>
th {
  color: rgb(66, 27, 0);
}
.Tablehead {
  display: flex;
  align-items: center;
  gap: 200px;
}
</style>
