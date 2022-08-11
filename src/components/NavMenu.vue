<script setup lang="ts"></script>

<template>
  <div class="nav">
    <slot></slot>
  </div>
</template>

<style scoped>
.nav {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 98%;
  height: 49px;
  padding: 10px;
  position: fixed;
  top: 0;
  background-color: rgb(250, 250, 250);
}
</style>
