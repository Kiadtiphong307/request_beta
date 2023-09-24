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
  {name: 'WTF Coffee Camp',  price:199, img:"https://scontent.fbkk4-2.fna.fbcdn.net/v/t39.30808-6/322884365_634904391740693_4185424965890588074_n.jpg?_nc_cat=110&ccb=1-7&_nc_sid=a2f6c7&_nc_eui2=AeFiZ4FtppUReF4nkdvzXgXJf5kvqfdMROF_mS-p90xE4UB-yzb0CSs6cc8LKKyfES92rauiaIJzr5-yGUe_EATo&_nc_ohc=EeRRAd16yZIAX-PWevL&_nc_zt=23&_nc_ht=scontent.fbkk4-2.fna&oh=00_AfAjOT3NsPR4TIBabOC_yVNOuDFAC0-CaPxUTCsJMBfGEQ&oe=65147A9A", quantity: 0 ,
    text_box:' ร้านคาเฟ่ที่มาแรงที่สุดในช่วนี้ไม่ว่าจะแพลตฟอร์มไหนก็แซงหน้าทุกร้านที่ผ่านมา ไม่ว่าจะเป็นเพราะการบริการหรือว่าคุณภาพในการชงกาแฟ และแน่นอนที่ขาดไปไม่ได้คือการตกแต่งร้านที่ทันสมัยและคุมโทนอบอุ่น ละมุนตาโดยออกแบบดพื่อคำนึงถึงความสบายใจและสบายตาของลูกค้าที่ไม่ว่าจะมาพักผ่อนหย่อนใจโดยการนั้งจิบกาแฟ หรือมาทำงาน  ก็พร้อมต้อนรับและบริการด้วยหัวใจ'
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
