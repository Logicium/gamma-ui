<script setup lang="ts">

import LeftIcon from "../assets/LeftIcon.vue";
import RightIcon from "../assets/RightIcon.vue";
import Panel from "@/components/Panel.vue";
import Map from "@/components/Map.vue";
import data from "./data.ts";
import Up from "../assets/Up.vue";
import Footer from "@/components/Footer.vue";
import Navbar from "@/components/Navbar.vue";


</script>

<template>
  <div id="home" class="webapp">

    <Navbar/>

    <div class="appTitle">
      <div class="est">EST. 2010</div>
      <div class="title">GAMMA KITCHEN</div>
    </div>

    <div class="imageWrap">

      <div class="imageArea">
        <div class="tagline">
          {{"Celebrate the vibrant flavors of New Mexico at Gamma Kitchen"}}
          <div class="controls">
            <div class="left"> <LeftIcon/> </div>
            <div class="right"> <RightIcon/> </div>
          </div>
        </div>
      </div>

    </div>

  </div>

  <Panel id="about" color="#157177" text="ABOUT" subtext="Tue - Sun | 10am - 8pm">
    <div class="infoArea">
      <div class="infoText">
        <div>{{data.about0}}</div>
        <div>{{data.about1}}</div>
        <div class="button-reverse">VIEW MENU</div>
      </div>
      <div class="infoImg"></div>
    </div>
  </Panel>

  <Panel id="location" color="#d97245" text="LOCATION" :subtext="data.address0">
    <div class="infoArea">
      <Map/>
      <div class="infoText">
        <div>{{data.location0}}</div>
        <div class="button-reverse">SEE REVIEWS</div>
      </div>
    </div>
  </Panel>

  <Panel id="contact" color="#efecd6" text="CONTACT" subtext="+1 585-010-0101">
    <div class="infoArea">

      <div class="contactInfo">
        <input type="text" placeholder="Name">
        <input type="email" placeholder="Email">
        <textarea placeholder="Message"/>
        <div class="button-reverse">SEND MESSAGE</div>
      </div>

      <div class="contactArea">
        <div class="contactItem">
          Get in touch to learn more about our menu, events, and catering.
        </div>
        <div class="contactItem face1"></div>
        <div class="contactItem face2"></div>
        <div class="contactItem click">
          <div class="cta">CALL US  <Up/></div>
        </div>
      </div>

    </div>

  </Panel>

  <Footer/>

</template>

<style scoped>

@media only screen and (max-width: 760px) {
  .infoArea{
    grid-template-columns: 1fr !important;
    grid-template-rows: 1fr 1fr;
    height: 100% !important;
  }
}

.click{
  cursor: pointer;
}

.face1{
  background-image: url("../assets/face5.avif");
}
.face2{
  background-image: url("../assets/face1.avif");
}

.cta{
  width: 100%;
  margin-top: auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  text-align: right;
  font-family: "BioRhyme", serif;

}

.contactItem,.contactInfo{
  padding: 2rem;
  display: flex;
  border-radius: 50px;
  background-color: #f2f1df;
  background-size: cover;
  background-position: 50% 100%;
}

.contactInfo{
  justify-content: space-between;
  flex-direction: column;
  text-align: right;
}

input,textarea{
  background-color: #f2f1df;
  border: none;
  border-bottom: 2px solid ;
  height: 4rem;
  font-size: 1.2vw;
  font-family: "Open Sans", serif;
}

textarea{
  height: 50%;
}

.contactItem{
  height: 100%;
  font-size: 2vw;
  line-height: 2vw;
  background-color: #157177;
  justify-content: end;
  color: #efecd6;
}

.contactArea{
  display: grid;
  width: 100%;
  height: 100%;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  grid-gap: 4rem;
}

.infoText, .infoImg{
  height: 100%;
  border-radius: 50px;
  font-size: 2vw;
}

.infoText{
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}

.infoImg{
  background-image: url("../assets/food3.jpg");
  background-size: cover;
  background-position: 40% 100%;

}

.infoArea{
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-gap: 4rem;
  width: 100%;
  height: 60vh;
  margin-top: 4rem;
}

.controls{
  display: flex;
}

.left,.right{
  display: flex;
  margin-top: 1vw;
  margin-right: 1vw;
  height: 4rem;
  width: 4rem;
  border-radius: 100%;
  background-color: #157177;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

.appTitle{
  display: flex;
  margin-top: 4rem;
  width: 100%;
  justify-content: space-between;
  font-size: 7vw;
  font-family: "BioRhyme", serif;
  line-height: 7vw;
  font-weight: 500;
}

.est{
  font-size: 2vw;
  font-weight: 500;
}

.title{
  text-align: right;
  width: 50%;
}

.imageWrap{
  display: flex;
  flex-direction: column;
}

.tagline{
  margin-top: auto;
  padding-top: 1vw;
  padding-right: 1vw;
  font-size: 2vw;
  height: auto;
  width: 40%;
  background-color: #efecd6;
  border-top-right-radius: 50px;
  transform: translateY(1rem);
}

.button{
  align-self: center;
  background-color: #157177;
  color: #efecd6;
  height: 4rem;
  width: 10rem;
  line-height: 4rem;
  border-radius: 2rem;
  text-align: center;
  cursor: pointer;
  font-size: calc(10px + 0.5vw);
}
.button-reverse{
  align-self: center;
  font-weight: 500;
  border: 2px solid black;
  height: 4rem;
  width: 10rem;
  line-height: 4rem;
  border-radius: 2rem;
  text-align: center;
  cursor: pointer;
  font-size: calc(10px + 0.5vw);
}

.webapp{
  display: flex;
  flex-direction: column;
  padding: 4rem;
}


.imageArea{
  display: flex;
  margin-top: 4rem;
  background-image: url("../assets/raton.jpg");
  background-size: cover;
  background-position: 100% 30%;
  width: 100%;
  height: 40vh;
  border-radius: 50px;
}

</style>
