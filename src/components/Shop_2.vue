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
  {name:'Yonma',  price:219, img:"https://scontent.fbkk4-4.fna.fbcdn.net/v/t39.30808-1/300499986_464925402210287_4974814192228614755_n.jpg?stp=dst-jpg_p320x320&_nc_cat=109&ccb=1-7&_nc_sid=754033&_nc_eui2=AeFwOhhorsKRdWyUI_kcSPCP1U8fL0lMUVnVTx8vSUxRWWpFD2E0t23ss2ddJ1j8fL9s2SotBhF7ffbU7jprAD0h&_nc_ohc=NQFghNqDedQAX9_OXtz&_nc_ht=scontent.fbkk4-4.fna&oh=00_AfAN6c071Fol30XgU5up4tF-Ydl7-PLl02rAp2iRPAyV-g&oe=6515B932", quantity: 0 ,
    text_box:'  ร้านกาแฟที่มาแรงที่สุดในช่วนี้ไม่ว่าจะแพลตฟอร์มไหนก็แซงหน้าทุกร้านที่ผ่านมา นั้นคือ i-love -coffe นั้นเอง ไม่ว่าจะเป็นเพราะการบริการหรือว่าคุณภาพในการชงกาแฟ และแน่นอนที่ขาดไปไม่ได้คือการตกแต่งร้านที่ทันสมัยและคุมโทนอบอุ่น ละมุนตาโดยออกแบบดพื่อคำนึงถึงความสบายใจและสบายตาของลูกค้าที่ไม่ว่าจะมาพักผ่อนหย่อนใจโดยการนั้งจิบกาแฟ หรือมาทำงาน '
    }])

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
