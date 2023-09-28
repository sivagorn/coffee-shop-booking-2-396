<template>
  <div class="box_all">
    <div class="col" v-for="(destination, index) in travelList" :key="index">
      <div class="card">
        <img :src="destination.img" class="card-img-top" alt="Travel Destination">
        <div class="card-body">
          <h3 class="card-title">{{ destination.name }}</h3>
          <p class="card-text">ราคาโต๊ะ: {{ destination.price }} บาท</p>
          <h6 class="card-subtitle">จำนวน 4 คนต่อ 1 โต๊ะ</h6>
          <button class="btn btn-primary" @click="reserveTable(destination.name, destination.quantity)">จองโต๊ะ</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>

import { ref } from 'vue';

const travelList = ref([
{name:'The Simple',    price:60, img:"https://cdn.chiangmainews.co.th/wp-content/uploads/2018/01/07083745/2-8-800x566.jpg", quantity: 0 ,
    text_box:'ความสุขคือกาแฟที่อร่อย และที่นี่มีมากมายให้เลือก! 🤩☕️ #กาแฟรสชาติพิเศษ'
    },
]);

</script>


<style scoped>
.card {
  height: 500px;
  width: 400px;
  margin: 20px;
  border: 1px solid rgb(255, 255, 255);
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(255, 255, 255, 0.1);
}

.card-img-top {
  object-fit: cover;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}

.card-body {
  text-align: center;
  padding: 20px;
}

.card-title {
  text-align: center;
  font-size: 1.5rem;
  margin-bottom: 10px;
}

.card-text {
  text-align: center;
  font-size: 1.2rem;
}

.card-subtitle {
  text-align: center;
  font-size: 1rem;
  color: #000000;
  margin-top: 10px;
}

.btn-primary {
  background-color: #83f368;
  border: none;
  border-radius: 5px;
  color: #000000;
}

.btn-primary:hover {
  background-color: #ff0000;
}

.box_all {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  margin: 30px;
}
</style>