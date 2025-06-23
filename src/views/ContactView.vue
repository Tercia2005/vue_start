<template>
    <div class="inpCard">
        <h1>Contact Us</h1> 
        <form @submit.prevent="handleSubmit">
            <input
                type="text" 
                v-model="name"
                placeholder="Enter you name" 
                required 
                />
            <br><br>
            <input 
              type="email" 
              v-model="email"
              placeholder="Enter a valid email address" 
              required
              />
              <textarea id="message" placeholder="Your message"></textarea>
            <br><br>
            <button type="submit">Submit</button>
        </form>

        <p v-if="submittedMessage" style="color: purple; margin-top: 10px;">{{ submittedMessage }}</p>
        </div>
</template>

<script>
export default {
    data(){
        return{
            name: '',
            email: '',
            submittedMessage:''
        };
    },
   methods:{
    handleSubmit(){
        const namePattern = /^[A-Za-z\s]{2,}$/;
        const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

        if (!namePattern.test(this.name)){
            this.submittedMessage = "Please enter a valid name.";
            return;
        }
            
        if (!emailPattern.test(this.email)){
            this.submittedMessage = "Please enter a valid email address.";
            return;

        }
        this.submittedMessage = 'Thank you, ' + this.name + '! We\'ll contact you soon!';

       
        this.name= '';
        this.email= '';
    
    }
   } 
};
</script>
<style scoped>
    .inpCard{
      width: 250px;
      min-height: 180px;
      border: 1px solid black;
      padding: 20px;
      margin: 0 auto; 
      text-align: center;
}

input {
  margin: 5px;
  padding: 8px;
  width: 200px;                
}
#message{

  width: 220px;
  height: 100px;      
  resize: vertical;  
  padding: 8px;
  font-size: 16px;
  box-sizing: border-box; 
}



button {
  padding: 8px 16px;
}


</style>