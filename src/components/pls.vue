<script setup>
defineProps({
  kakashka: String,
})
let Name = {{kakashka}}
function Add() {
  console.log(Name)
}
</script>
<template>
  <button @click="Add">{{ kakashka }}</button>
</template>
