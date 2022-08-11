<script lang="ts" setup></script>

<template>
  <div class="lastDocsContainer">
    <slot></slot>
  </div>
</template>

<style scoped>
.lastDocsContainer {
  /* width: 511px*/
  width: 700px;
  margin-left: 165px;
  margin-top: 5px;
  display: grid;
  grid-template-columns: repeat(6, 205px);
  grid-template-rows: minmax(260px, auto);
  gap: 14px;
}
</style>
