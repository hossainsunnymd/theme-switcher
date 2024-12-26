<script setup>

import { data } from '../data/data.js'

function update(value) {
  
    data.bgcolor = value;
    data.textColor = value;
    data.buttonBgColor = value;
    data.buttonText = value;
    
 
    localStorage.setItem('theme', JSON.stringify(data));
}


</script>

<template>
<div class="m-10">
    <select @change="update($event.target.value)" class="px-5">

        <option value=""></option>
        <option value="green">Green</option>
        <option value="blue">Blue</option>
        <option value="red">Red</option>
        <option value="yellow">Yellow</option>
    </select>
</div>
</template>

<style>
/* Your styles here */
</style>
