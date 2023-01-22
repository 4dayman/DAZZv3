<template>
  <div class="home">
    <MainSlider/>
    <MainDesc/>
    <Services/>
    <SubServices/>
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <h1 class="text">DAZZ</h1>
    <div class="call_btn">
      <CallBtn/>
    </div>
    <!-- <marquee behavior="scroll" direction="left" loop>Some text Some text Some text</marquee> -->
  </div>
</template>

<script>
// @ is an alias to /src
import MainSlider from '@/components/MainSlider'
import MainDesc from '@/components/MainDesc'
import Services from '@/components/Services'
import SubServices from '@/components/SubServices'
import CallBtn from '@/components/UI/CallBtn'
export default {
  name: 'HomeView',
  components: {
    MainSlider, 
    CallBtn,
    MainDesc,
    Services,
    SubServices,

  }
}
</script>

<style lang="scss" scoped>
.home{
  position: relative;
  padding-top: 80px;
  @media (max-width: 360px) {
    padding-top: 55px;
  }
}
.text{
  font-size: 60px;
  font-weight: 400;
  color: #c0c0c0;
  font-family: Vogue serif;
  text-shadow: 1px 1px 2px gray, 0 0 1em rgb(201, 201, 204), 0 0 0.2em rgb(162, 162, 173);
}
.call_btn{
  z-index: 1;
  position: fixed;
  bottom: 80px;
  right: 20px;
}
</style>
