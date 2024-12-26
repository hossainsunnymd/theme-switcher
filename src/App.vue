<script setup>
import { onMounted } from 'vue'
 import {data } from './data/data.js'
 import ThemeSwitcher from './components/ThemeSwitcher.vue'
 onMounted(() => {
   
    const storedata = localStorage.getItem('theme');
    if (storedata) {
      
        Object.assign(data, JSON.parse(storedata));
    }
})
</script>

<template>
  <theme-switcher/>
  <div :class="`bg-${data.bgcolor}-500 text-${data.textColor} p-10 max-w-[1300px] mx-auto mt-10`">
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Officia nemo unde libero repudiandae soluta ea hic tempore excepturi maiores explicabo saepe sed commodi quae architecto error voluptates dolorem, eum aspernatur!
    </p>
  </div>

</template>

<style scoped>

</style>
