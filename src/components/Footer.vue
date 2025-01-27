<script setup lang="ts">

</script>

<template>

  <div class="footerWrap">
    <div class="footer">
      <div class="title">GAMMA KITCHEN</div>
      <div class="socials">
        <div class="social">FACEBOOK</div>
        <div class="social">INSTAGRAM</div>
        <div class="social">SHARE</div>
      </div>
    </div>

    <div class="info">
      <div class="rights">@2025</div>
      <div class="rights">All Rights Reserved</div>
    </div>

  </div>

</template>

<style scoped>

@media (max-width: 760px) {
  .socials {
    flex-direction: column;
    text-align: right;
  }
}

.socials{
  margin-top: auto;
  display: flex;
  justify-content: space-between;
  width: 30%;
}

.social{
  cursor: pointer;
  font-weight: 500;
  margin-left: 1vw;
  font-family: "BioRhyme", serif;
}

.info{
  display: flex;
  padding-top: 1vw;
  margin-top: 1vw;
  border-top: 2px solid #efecd6;
  justify-content: space-between;
}

.footerWrap{
  border-top-left-radius: 50px;
  border-top-right-radius: 50px;
  display: flex;
  flex-direction: column;
  background-color: #4a221a;
  color: #efecd6;
  width: 100%;
  padding: 4rem;
  padding-bottom: 1vw;

}

.footer{
  height: 20vh;
  position: relative;
  display: flex;
  justify-content: space-between;
}

.rights{
  font-size: calc(10px + 0.5vw);
  margin-top: auto;
  font-weight: 500;
}

.title{
  //color: #653025;
  font-family: "BioRhyme", serif;
  font-size: 7vw;
  line-height: 7vw;
  margin-top: auto;
  width: 40%;
}

</style>
