<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Ordering Sytem</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">

        <ion-toolbar>
          <ion-title size="large">"Ecommerce Brand"</ion-title>
        </ion-toolbar>
      </ion-header>
    
      <ion-content>

      <ion-card id="centerImage">
        <img src="https://assetsio.reedpopcdn.com/g502x_f9QuuM8.jpeg?width=1600&height=900&fit=crop&quality=100&format=png&enable=upscale&auto=webp">
        <ion-card-header>
          <div class="centur">
          <ion-card-title>$250</ion-card-title>
          <ion-card-title>Mouse</ion-card-title>
        </div>
      </ion-card-header>
      <div class="centur">
        <ion-input v-model="num4" placeholder="Enter Quantity" >
       
      </ion-input>
       <ion-button fill="solid" expand="block" size="default" @click="mouse1()">Buy: {{ num1 }}</ion-button>
      </div>
      </ion-card>

      <ion-card id="centerImage">
        <img src="https://cdn.thewirecutter.com/wp-content/media/2023/03/mechanicalkeyboards-2048px-4906-2x1-1.jpg?auto=webp&quality=75&crop=2:1&width=1024">
        <ion-card-header>
          <div class="centur">
          <ion-card-title>$300</ion-card-title>
          <ion-card-title>Mechanical Keyboard</ion-card-title>
        </div>
      </ion-card-header>
      <div class="centur">
        <ion-input v-model="num5" placeholder="Enter Quantity" > 
      
        </ion-input>
        <ion-button fill="solid" expand="block" size="default" @click="keyboard1()">Buy: {{ num2 }}</ion-button>
       </div>
      </ion-card>

      <ion-card id="centerImage">
        <img src="https://www.pcgamesn.com/wp-content/sites/pcgamesn/2022/05/alienware-aw3423dw-review-the-ultimate-hdr-gaming-monitor.jpg">
        <ion-card-header>
          <div class="centur">
          <ion-card-title>$2500</ion-card-title>
          <ion-card-title>Monitor</ion-card-title>
        </div>
      </ion-card-header>
     
      <div class="centur">
        <ion-input v-model="num6" placeholder="Enter Quantity" > 
       
        </ion-input>
        <ion-button fill="solid" expand="block" size="default" @click="monitor1()">Buy: {{ num3 }}</ion-button>
       </div>
      </ion-card>
      
      <ion-card>
        <ion-card-header>
          <ion-title> Order Summary</ion-title>
        </ion-card-header>
        <ion-button fill="solid" expand="block" size="default" @click="total()">TOTAL</ion-button>
        <ion-card-content>
        <h1>Ordered Mouse : {{ num1 }}</h1>
        <h1>Ordered Monitor : {{ num2 }}</h1>
        <h1>Ordered Keyboard : {{ num3 }}</h1>
        <h1> TOTAL: {{ Sum }}</h1>

      </ion-card-content>
      </ion-card>
    </ion-content>

    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">

import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonInput } from '@ionic/vue';
import {remove,add,} from 'ionicons/icons';
import {ref} from 'vue';




const monitor = ref(2500);
const mouse = ref (250);
const keyboard = ref (300) ;

const num1 = ref("");
const num2= ref("");
const num3 =ref("");

const num4 = ref("");
const num5= ref("");
const num6 =ref("");
const Sum=ref("");



function mouse1() {
  num1.value =((Number(mouse.value) *Number(num4.value))).toString();
}


function keyboard1() {
  num2.value =((Number(keyboard.value) *Number(num5.value))).toString();
}


function monitor1(){
  num3.value=((Number(monitor.value)*Number(num6.value))).toString();
}
function total(){
 Sum.value =((Number(num1.value)+ Number(num2.value)+Number(num3.value))).toString();
}
</script>

<style scoped>
.centur{
  text-align: center;
  font-size: 25px;

}
</style>