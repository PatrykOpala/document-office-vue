<script setup lang="ts">

</script>

<template>
  <div class="chooseField">
    <p class="chooseFieldParagraph">Należące do kogokolwiek</p>
    <div class="chooseFieldOption">
        <!-- <div>Należące do kogokolwiek</div> -->
        <!-- <div>Należące do mnie</div>
        <div>Nienależące do kogokolwiek</div> -->
    </div>
</div>
</template>

<style scoped>
/*
width: 190px;
height: 25px;
*/

.chooseField{
    position: absolute;
    top: 285px;
    width: 220px;
    z-index: 90;
    background-color: transparent;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.chooseField > .chooseFieldParagraph{
    display: block;
    width: 190px;
    height: 25px;
    text-align: center;
    line-height: 28px;
    padding: 0 5px;
    border-radius: 4px;
    margin-left: 60vw;
}

.chooseField > .chooseFieldParagraph:hover{
    background: rgba(48, 47, 47, 0.151);
    cursor: pointer;
}

.chooseFieldOption{
    width: 99%;
    min-height: 40px;
    background-color: #fff;
    margin-top: -10px;
    display: none;
    flex-direction: column;
    border-radius: 4px;
    box-shadow: 0 3px 10px 2px rgba(48, 47, 47, 0.281);
}

.chooseFieldOption > div{
    height: 20px;
    margin-top: 5px;
    padding: 6px;
    font-size: 13px;
    line-height: 20px;
}

.chooseFieldOption > div:hover{
    cursor: pointer;
    background: rgba(48, 47, 47, 0.151);
}
</style>