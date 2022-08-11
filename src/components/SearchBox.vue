<script setup lang="ts"></script>

<template>
  <div class="searchBox">
    <button>
      <img src="@/assets/search-icon-32x32.svg" alt="" srcset="" />
    </button>
    <input type="text" placeholder="Szukaj" class="szukajka" />
    <button><img src="@/assets/cancel-icon-32x32.svg" /></button>
  </div>
</template>
<style scoped>
.searchBox {
  width: 38vw;
  height: 45px;
  border-radius: 6px;
  background: rgba(230, 230, 230, 0.685);
  padding: 2px;
  display: flex;
  flex-direction: row;
  align-items: center;
}

/* offsetWidth - 38 */
/* offsetHeight - 38 */
/* #3c3c3c */

.searchBox > button {
  border-radius: 50px;
  margin-left: 3px;
  width: 32px;
  height: 32px;
  padding: 20px;
  border: none;
  outline: none;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: transparent;
}

.searchBox > button:not(:first-child) {
  border-radius: 50px;
  margin-right: 3px;
  width: 32px;
  height: 32px;
  padding: 20px;
  border: none;
  outline: none;
  align-items: center;
  justify-content: center;
}

.searchBox > button:hover {
  background: rgba(70, 70, 70, 0.1);
  cursor: pointer;
}

.searchBox > .szukajka {
  font-size: 1rem;
  width: 87%;
  border: none;
  outline: 1px solid transparent;
  background: transparent;
}
</style>
