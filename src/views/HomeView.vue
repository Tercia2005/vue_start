<template>
  <h1>This is an home page</h1>
  <button @click="opinion = !opinion">Change Opinion</button>
  <h1 v-if="opinion">Vue is Awesome!</h1>
  <h1 v-else>Vue is aight</h1>
<h2>{{greeting() }}</h2>
<h2>{{ greet }}</h2>
<div>
  <p> {{ count }}</p>
  <button @click="increase()">+</button>
  <button @click="decrease()">-</button>
</div>
<img :src="url" alt="cat">
</template>
 
<script>
export default{
 data() {
  return {
    firstName: "Tercia",
    favColor: null,
    count: 0,
    url:"https://t3.ftcdn.net/jpg/02/36/99/22/360_F_236992283_sNOxCVQeFLd5pdqaKGh8DRGMZy7P4XKm.jpg",
    opinion: true,
  }

 }, methods: {
    greeting(){
      return 'Hello There ' + this.firstName
    },
    decrease(){
      if (this.count > 0) {
        this.count --;
      }
    },
    

    increase(){
      this.count++;
    }
  
 }, computed: {
    greet() {
      return "Hi"
    }
 }
}


 
</script>

<style scoped>
h1{
  color: purple;
}
</style>
