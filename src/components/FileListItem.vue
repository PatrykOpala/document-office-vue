<script lang="ts" setup>
import { ref, onMounted } from "vue";
const props = defineProps<{
  fName: string;
}>();
let fNameFirstLetter = ref("");
onMounted(() => {
  if (props.fName !== "") {
    fNameFirstLetter.value = props.fName[0];
  }
});
</script>

<template>
  <div class="docsCards">
    <div class="docsCardsImg">
      <div class="cardsImg">{{ fNameFirstLetter }}</div>
    </div>
    <div class="dCLapse">
      <div class="left">
        <span class="fileName">{{ props.fName }}</span>
        <span class="timelapse">Data</span>
      </div>
      <div class="right">
        <button>
          <img src="../assets/option-icon-24x24.svg" alt="option_icon" />
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.docsCards {
  min-height: 28vh;
  height: 40vh;
  border: 1px solid rgba(49, 49, 49, 0.205);
  border-radius: 3px;
}

.docsCards:hover {
  border: 0.3px solid rgba(30, 180, 30, 0.9);
  cursor: pointer;
}

.docsCards > .docsCardsImg {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 70%;
  border-bottom: 1px solid rgba(49, 49, 49, 0.205);
}

.docsCards > .docsCardsImg > .cardsImg {
  width: 50px;
  height: 50px;
  background-color: rgba(30, 180, 30, 0.9);
  border-radius: 3px;
  text-align: center;
  line-height: 50px;
  font-size: 34px;
  color: #fff;
}

.docsCards > .dCLapse {
  display: grid;
  grid-template-columns: 88% 12%;
  width: 96%;
  height: 25%;
  /* background-color: aqua; */
  margin: 3% 2%;
}


.docsCards > .dCLapse > .right{
  /* background-color: antiquewhite; */
  /* position: absolute; */
}

.docsCards > .dCLapse > .left > span {
  display: block;
  width: 110px;
  font-weight: 550;
  font-size: 14px;
  text-overflow: ellipsis;
  white-space: nowrap;
  color: rgba(0, 0, 0, 0.8);
  padding: 5px;
  margin-left: 4%;
}

.docsCards > .dCLapse > .left > .fileName{
  margin-top: 17%;
}

.docsCards > .dCLapse > .left > .timelapse {
  margin-top: 4%;
}

.docsCards > .dCLapse > .right > button {
  width: 33px;
  height: 33px;
  border: none;
  outline: none;
  border-radius: 80%;
  background-color: transparent;
  margin: 40% 0;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  top: 51%;
  right: 40%;
}

.docsCards > .dCLapse > .right > button:hover {
  background: rgba(48, 47, 47, 0.151);
}
</style>
