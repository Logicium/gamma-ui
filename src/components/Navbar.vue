<script setup lang="ts">

import {nextTick} from 'vue';

const scrollToRef = (id:string) => {
  nextTick(() => {
    console.log(window?.document?.getElementById(id));
    window?.document?.getElementById(id)?.scrollIntoView({behavior:"smooth"})
  });
};

</script>

<template>

  <div class="navbar">
    <div class="appIcon"><div>G</div></div>
    <div class="navItems">
      <div class="item">HOME</div>
      <div class="item" @click="scrollToRef('about')">ABOUT</div>
      <div class="item" @click="scrollToRef('location')">LOCATION</div>
      <div class="contact" @click="scrollToRef('contact')">CONTACT US</div>
    </div>
  </div>

</template>

<style scoped>

@media (max-width: 760px) {
  .navItems{
    width: 80% !important;
  }
  .contact{
    width: 4rem !important;
  }
}

.navbar{
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.item{
  cursor: pointer;
  margin-right: 1vw;
}

.contact{
  background-color: #157177;
  color: #efecd6;
  height: 4rem;
  width: 10rem;
  line-height: 4rem;
  border-radius: 2rem;
  text-align: center;
  cursor: pointer;
}

.navItems{
  width: 40%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.appIcon{
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #157177;
  color:#efecd6;
  height: 4rem;
  width: 4rem;
  font-weight: 600;
  border-radius: 100%;
  font-size: calc(20px + 2vw);
  font-family: "BioRhyme", serif;
  cursor: pointer;
}

</style>
