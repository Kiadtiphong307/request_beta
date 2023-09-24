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
  {name:'Cat Brothers Cafe',  price:169, img:"https://scontent.fbkk3-2.fna.fbcdn.net/v/t39.30808-6/208650936_1893154220864701_2114485125737848224_n.jpg?_nc_cat=104&ccb=1-7&_nc_sid=a2f6c7&_nc_eui2=AeFITXNBfXrMxj2j0bpQON1UO0Z8nVHpTYw7RnydUelNjHgfdQmrIAIbwzX1xh1k5SgO8pYZp2zWtk7iRgmVZ66c&_nc_ohc=KBkMaufmLikAX9hsSxB&_nc_zt=23&_nc_ht=scontent.fbkk3-2.fna&oh=00_AfC-iSKlTdx3qvyRr3k_pXNiNmkZminjdFHp_vH0wgI39A&oe=6514EB12", quantity: 0 ,
    text_box:' คาเฟ่แมวที่พร้อมฮีลใจของคุณไม่ว่าจะผ่านอะไรมา ก็จะมีน้องแมวเหมียวมากหน้าหลายตามารอพร้อมบริการคุณอย่างเต็มความสามารถเพียงให้ขนมและอาหารที่เจ้านายชอบ!!'
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
