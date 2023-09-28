<script setup>

import { RouterView } from 'vue-router'
import boxheader from '@/views/boxheader.vue'
import JumboHead from './views/JumboHead.vue'
</script>


<template>
  <div class="container">
    <boxheader></boxheader>
    <JumboHead
      class="jumbo-head"
      text_title="It's tea time 🍰🧋🏕"
      ex_box="บรรยากาศกาแฟที่ดี จองง่ายๆ แค่คลิกเดียว"
    ></JumboHead>
    <RouterView />
  </div>
</template>

<script>
export default {
  name: 'App',
};
</script>

<style scoped>
.jumbotron {
  background-color: #007BFF;
  color: #fff; 
  padding: 2rem;
  border-radius: 15px; 
}

.display-4 {
  font-weight: bold; 
}

.lead {
  font-size: 1.25rem; 
}

body {
  background-color: #ffffff; 
}

.container {
  background-color: #e7c7a8;
  padding: 12px;
  border-radius: 25px; 
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
}

</style>



