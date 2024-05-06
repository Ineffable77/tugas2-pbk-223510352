<script setup>
import { ref } from 'vue';

const text = ref('')

function inp(e){
  text.value = e.target.value
}

const sub = ref('')

const nama = ref('name')
</script>

<template>
  <div class="inputBox">
    <input :value="text" @input="inp"  required="required">
    <span>Nama kamu</span>
  </div>
   
    <button @click="sub = text" class="button-1" role="button">submit</button>
    
    
    <h2 :class="nama"> {{ sub }}</h2>
  
    


</template>

<style>
.name {
  color: red;
}


.button-1 {
  background-color: #5b63d3;
  border-radius: 8px;
  border-style: none;
  box-sizing: border-box;
  color: #FFFFFF;
  cursor: pointer;
  display: inline-block;
  font-family: "Haas Grot Text R Web", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 14px;
  font-weight: 500;
  height: 40px;
  line-height: 20px;
  list-style: none;
  margin: 0;
  outline: none;
  padding: 10px 16px;
  position: relative;
  text-align: center;
  text-decoration: none;
  transition: color 100ms;
  vertical-align: baseline;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  margin-top: 1.5rem;
  margin-bottom: 1rem;
}

.button-1:hover,
.button-1:focus {
  background-color: #c01212;
}



</style>