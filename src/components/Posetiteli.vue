<script setup>
import { ref } from 'vue'
const props = defineProps({
  AddVisiter: Function,
  Name: String,
  Company: String,
  Group: String,
  Presence: Boolean,
})
let kakjetak = props.Name
console.log(kakjetak)
const NewVisiter = {
  Name: '',
  Group: '',
  Company: '',
  Presence: false,
  Id: 10,
}

const AddVisiter = () => {
  NewVisiter.Name = Name.value
  NewVisiter.Group = Group.value
  NewVisiter.Company = Company.value
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
</script>
