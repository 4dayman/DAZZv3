<template>
<Header/>
  <router-view/>
<Footer/>
</template>

<script>
import Header from '@/components/Header'
import Footer from '@/components/Footer'
export default {
  name: 'HomeView',
  components: {
    Header,
    Footer,
  }
}
</script>


<style lang="scss">
@import '@/fonts/fonts.css';
@import '@/assets/nullstyle.scss';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
nav {
  // padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
h2{
  font-weight: 700;
  font-size: 40px;
  line-height: 140.5%;
  color: #41456B;
}

h3{
  font-weight: 700;
  font-size: 25px;
  line-height: 140%;
  letter-spacing: 0.02em;
  color: #41456B;
}
h4{
  font-weight: 700;
  font-size: 15px;
  line-height: 140%;
  letter-spacing: 0.02em;
  color: #41456B;
}
</style>
