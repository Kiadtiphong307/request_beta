<template>
  <div class="box_all">
  <div class="col" v-for="(n,i) in travelList" :key="n">
    <div class="card" style="width: 25rem;" >
      <img :src="n.img" class="card-img-top">
      <div class="card-body">
        <h3 class="card-title">{{ n.name }}</h3>
        <p>ราคาค่าเข้า : {{n.price}}</p>

        <a class="btn btn-primary" @click="list_local_control(i.name, i.quantity)"> จองบัตร </a>
      </div>
    </div>
  </div>
</div>

</template>


<script setup>

import { ref } from 'vue';

const travelList=ref([
  {name:'PIZZA PHU PING ',      price:149, img:"https://scontent.fbkk3-3.fna.fbcdn.net/v/t39.30808-1/279237363_384930236981634_4493984021961394939_n.jpg?stp=dst-jpg_p320x320&_nc_cat=103&ccb=1-7&_nc_sid=754033&_nc_eui2=AeGionZ0HbBxPlleYosduaMHz7TXIPFEZv_PtNcg8URm__GxmzGYNsF7_AnAwWjYcCu7_s7r6c7qY5mVCiqSAM-9&_nc_ohc=6QC5UoOXl4wAX87suRt&_nc_ht=scontent.fbkk3-3.fna&oh=00_AfDLichat1DqXi0NiezhyX6q-QHi-jtTOukNK2CrKe59ww&oe=6515D103", quantity: 0 ,
    text_box:'  ร้านพิซซ่าที่พร้อมให้ความอิ่มอร่อยกับคุณไม่อั้น ไม่ว่าจะที่ไหนเพราะเรามีบริการส่งถึงบ้าน หรือคุณจะมานั้งทานที่ร้านก็ได้ร้านก็มีพื้นที่เพียงพอที่จะต้อนรับลูกค้าคนพิเศษแบบคุณ '
    },])


</script>

<style>

.card-img-top{
height: 100%;
padding: 25px;

}
.box_all{
justify-content: center;
align-items: center;
margin-left: 30%;
text-align: center
}

</style>
