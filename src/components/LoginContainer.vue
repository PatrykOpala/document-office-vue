<script setup lang="ts">
// defineProps<{
//   msg: string
// }>()

import {useRouter} from "vue-router"
const route = useRouter()

function testLogin(){
  route.push({path: "/dashboard"})
}
</script>

<template>
  <div class="LoginContent">
    <div class="Logo">Document<span>Office</span></div>
    <p class="z">otwórz dokumenty</p>
    <div class="form">
        <label class="labelc">Adres E-mail</label>
        <input type="text"/>
    </div>
    <div class="form">
        <label class="labelc">Hasło</label>
        <input type="password"/>
    </div>
    <div class="bZal">
        <button class="bTwo">utwórz konto</button>
        <button @click="testLogin">zaloguj się</button>
    </div>
</div>
</template>

<style scoped>
.LoginContent{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 440px;
    border: 1px solid rgba(140, 140, 140, 0.3);
    margin-top: 20vh;
    border-radius: 8px;
    margin-left: auto;
    margin-right: auto;
}

.LoginContent > .Logo{
    font-size: 2rem;
    font-family: sans-serif;
    margin-top: 40px;
}

.LoginContent > .Logo > span{
    margin-left: 5px;
    font-weight: 700;
    color: rgba( 30, 180, 30, 0.9);
}

.LoginContent > .z::first-letter,
.LoginContent > .bZal > button::first-letter{
    text-transform: uppercase;
}

.LoginContent > .z{
    margin-top: 17px;
    margin-bottom: 10px;
    font-size: 1.5rem;
}

.LoginContent > .form{
    position: relative;
    margin-top: 30px;
    margin-bottom: 10px;
    border: 1px solid rgba(140, 140, 140, 0.3);
    width: 70%;
    padding: 20px;
    border-radius: 6px;
}

.LoginContent > .form > input{
    width: 97%;
    border: none;
    outline: none;
    font-size: 1.2rem;
}

.form > .labelc{
    position: absolute;
    top: -8px;
    pointer-events: none;
    background: #fff;
    padding-left: 5px;
    padding-right: 5px;
    font-size: 0.8rem;
}

.LoginContent > .bZal{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    margin-top: 20px;
    margin-bottom: 30px;
}

.LoginContent > .bZal > button{
    background: rgba( 30, 180, 30, 0.9);
    color: #fff;
    border: none;
    border-radius: 3px;
    padding: 10px;
    font-weight: 600;
}

.LoginContent > .bZal > .bTwo{
    background: transparent;
    color: rgba( 30, 180, 30, 0.9);
}

.LoginContent > .bZal > .bTwo:hover{
    background: transparent;
    color: rgba(25, 155, 25, 0.9);
}

.LoginContent > .bZal > button:not(:first-child){
    margin-left: 160px;
}

.LoginContent > .bZal > button:hover{
    background: rgba(25, 155, 25, 0.9);
    cursor: pointer;
}
</style>