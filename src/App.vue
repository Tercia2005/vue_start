<template>
  <aside :id="styling" >

    <NavbarComp/> 
    
    
    <router-view/>
  </aside>
  
</template>
<script>
import NavbarComp from './components/NavbarComp.vue'

export default{
  components: {
    NavbarComp
},
data(){ 
  return{
   styling:""
  }
},  
methods:{ 
  changeBackground(){ 
    if(this.$route.path == '/employee'){
      this.styling = "background" 
    } else{
      this.styling = "" 
    }
  }
},
watch:{
  $route(newValue){
    this.changeBackground()
  }
},
mounted(){
  this.changeBackground()  
}

}
</script>
<style>
#background{
  background: url("https://www.shutterstock.com/shutterstock/photos/2286554497/display_1500/stock-photo-random-pictures-cute-and-funny-2286554497.jpg");
}

#app {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
