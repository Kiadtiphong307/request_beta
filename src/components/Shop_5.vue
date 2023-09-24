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

{name:'Box Box Dog Cafe ',     price:299, img:"https://scontent.fbkk3-3.fna.fbcdn.net/v/t39.30808-6/326455096_503747178550404_6148717715410575457_n.jpg?_nc_cat=103&ccb=1-7&_nc_sid=a2f6c7&_nc_eui2=AeFUY4RKPwA947rwJwBEF92kYzQdwwD2v4JjNB3DAPa_gms09JN5e2X_yOI3duG7twTwPIsM0ZNIhsS_vqdVIcli&_nc_ohc=hbuPUb55KUkAX_iS2Qf&_nc_zt=23&_nc_ht=scontent.fbkk3-3.fna&oh=00_AfA54glGiurX303uIsko2ZK3VE35bYBbTzWRCDbV3HPfHQ&oe=6513EAA8", quantity: 0 ,
    text_box:' คาเฟ่น้องมะหมาสุดน่ารักไม่ว่าจะสายพันธุ์เล็ก-ใหญ่ที่พร้อมคลอเคียเพื่อลดและขจัดความเหนื่อยล้าจากการทำงานที่มีระบบทุนนิยมเป็นตัวชี้วัดในความสำเร็จ มาหาเราสิ เรามีน้องหมาที่น่ารักพร้อมให้บริการคุณไม่ว่าจะเป็นน้องหมาสายพันธุ์ไหน!!'
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
