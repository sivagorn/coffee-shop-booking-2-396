<template>
<div class="row mb-2">
        <div class="col-md-6" v-for="(n,i) in travelList" :key="n">
          <div class="row g-0 border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative">
            <div class="col p-4 d-flex flex-column position-static">
              <strong class="d-inline-block mb-2 text-primary-emphasis">ร้านที่ {{ i+1 }} </strong>
              <h3 class="mb-0">{{n.name}}</h3>
              <div class="mb-1 text-body-secondary">ราคาต่อโต๊ะ {{n.price}} บาท</div>
              <p class="card-text mb-auto">{{n.text_box}}</p>
              
              <div style="margin-bottom: 30px;">
              <RouterLink :to="{name: `news_${i+1}` , params: {id: n.name}}" class="icon-link gap-1 icon-link-hover stretched-link">
               รายละเอียดเพิ่มเติม
                <svg class="bi"> <use xlink:href="#chevron-right"/></svg>
             </RouterLink>
            </div>     
            </div>
            <div class="col-auto d-none d-lg-block">
              <svg class="bd-placeholder-img" width="200" height="250" xmlns="http://www.w3.org/2000/svg" role="img"  preserveAspectRatio="xMidYMid slice" focusable="false" 
              style="margin: 15px;" >
                <image :xlink:href="n.img" x="0" y="10" width="200" height="200" />
              </svg>
            </div>
          </div>
        </div>
    </div>
</template>

<script setup>

import { RouterLink } from 'vue-router'
import { ref } from 'vue';

const travelList=ref([
   {name: 'The Caferista',  price:50, img:"https://cdn.chiangmainews.co.th/wp-content/uploads/2018/01/07083746/1-8-800x566.jpg", quantity: 0 ,
    text_box:'เริ่มวันด้วยกาแฟที่นี่ แล้ววันนี้จะสดใสมากขึ้น ☕️ #ร้านกาแฟโปรด'
    }, 
  
    {name:'The Simple',    price:60, img:"https://cdn.chiangmainews.co.th/wp-content/uploads/2018/01/07083745/2-8-800x566.jpg", quantity: 0 ,
    text_box:'ความสุขคือกาแฟที่อร่อย และที่นี่มีมากมายให้เลือก! 🤩☕️ #กาแฟรสชาติพิเศษ'
    },
    
    {name:'ฮักมาว แม่โจ้',   price:50, img:"https://cdn.chiangmainews.co.th/wp-content/uploads/2018/01/07083745/3-11-800x566.jpg", quantity: 0 ,
    text_box:'นั่งกินกาแฟ มีความสุข และกับบรรยากาศสุดเพลิดเพลิน 🌞☕️ #แรงบันดาลใจ'
    },
    
    {name:'Have-A-Hug',     price:50, img:"https://cdn.chiangmainews.co.th/wp-content/uploads/2018/01/07083744/4-10-800x566.jpg", quantity: 0 ,
    text_box:'สัมผัสความอบอุ่นในแก้วกาแฟนี้ รับรองไม่ผิดหวัง! ☕️❤️ #ความอร่อย'
    },
    
    {name:'Café Woodhouse',  price:45, img:"https://cdn.chiangmainews.co.th/wp-content/uploads/2018/01/07083744/5-10-800x566.jpg", quantity: 0 ,
    text_box:'ร้านนี้เหมาะสำหรับกาแฟเลิศรส และชิลล์มาก! 😌☕️ #คาเฟ่ชิลล์'
    },
    
    {name:'Imagines House',  price:50,  img:"https://cdn.chiangmainews.co.th/wp-content/uploads/2018/01/07083743/6-8-800x566.jpg", quantity: 0 ,
    text_box:'เพิ่งค้นพบสถานที่ที่จะร่วมสนุกกับเพื่อนและกาแฟในราคาสบายกระเป๋า ☕️👯‍♂️ #กาแฟกับเพื่อน'
    },
])


</script>

<style>
  .row {
    background-color: #f5f5f5; 
  }

  h3 {
    color: #333; 
  }
  .row {
    background-color: #f5f5f5;
    padding: 20px;
    margin-bottom: 20px; 
  }

  h3 {
    color: #333;
    font-size: 24px; 
  }

  .row {
    background-color: #c5ddb4;
    padding: 20px; 
  }

  h3 {
    color: #333;
    font-size: 24px;
  }

  .icon-link {
    text-decoration: none; 
    color: #0084ff;
    transition: color 0.2s;
  }

  .icon-link:hover {
    color: #ff0000; 
  }
  
  .shadow-box {
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.2); 
  }



</style>

