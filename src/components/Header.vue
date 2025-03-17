<script setup></script>
<template>
  <div>
    <div>
      <div class="Header">
        <img src="/logo.svg" />
        <input class="FindInput" placeholder="Поиск по имени" />
        <img class="FindButton" src="/ButtonAdd.svg" />
        <h1 class="right">Посетители</h1>
      </div>
    </div>
  </div>
</template>
<style scoped>
.right {
  position: absolute;
  padding-right: 30px;
  padding-top: 30px;
  right: 1px;
  top: 1px;
  color: rgb(66, 27, 0);
}
.Header {
  display: flex;
  gap: 20px;
  align-items: center;
}
.FindInput {
  width: 30vh;
  height: 4vh;
  border-color: gray;
  outline: none;
  border-radius: 5px;
  background-color: white;
  border: none;
  filter: drop-shadow(0px 1px 4px rgba(0, 0, 0, 0.161));
}
.FindButton {
  height: 4vh;
}
.FindButton:hover {
  cursor: pointer;
}
</style>
