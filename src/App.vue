<template>
  <div id="app">
    <Header></Header>    
    <Quotes></Quotes> 
    <Footer></Footer>   
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Quotes from "./components/Quotes.vue";

export default {
  name: "app",
  components: {
    Quotes,
    Header,
    Footer
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;  
  background-color: rgb(247, 193, 122);
  margin:0px;
}

</style>
