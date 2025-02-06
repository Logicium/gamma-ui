<script setup lang="ts">
defineProps(["id",'color','text','subtext']);
</script>

<template>

  <div class="panel" :id="id">
    <div class="info">
      <div>{{text}}</div>
      <div class="subtext">{{subtext}}</div>
    </div>
    <slot/>
  </div>
  <div class="foot"></div>

</template>

<style scoped>

@media (max-width: 760px) {
  .info {
    flex-direction: column;
  }
  .panel{
    height: 100%;
  }

  .foot{
    height: 10rem !important;
  }

}

.foot{
  background-color: v-bind(color);
  height: 8rem;
  width: 100%;
  margin-bottom: -4rem;
}

.panel{
  width: 100%;
  padding: 4rem;
  border-top-left-radius: 50px;
  border-top-right-radius: 50px;
  background-color: v-bind(color);
  margin-bottom: -1px;
}

.info{
  font-family: "BioRhyme", serif;
  font-size: 7vw;
  line-height: 7vw;
  display: flex;
  justify-content: space-between;
  width: 100%;
}

.subtext{
  font-size: 2vw;
  line-height: 4vw;
}

</style>
