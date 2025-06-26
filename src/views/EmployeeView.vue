<template >
  <div class="section">
    <form @submit.prevent="handleSubmit">
        <h2>LEAVE REQUEST</h2>
        <br>
        
        <div class="mb-3 input" >
          <label for="employeeNum" class="form-label">Employee name: </label>
          <input type="text" class="form-control" id="employeeName" aria-describedby="" v-model="EmpName">
          
        </div>
        <div class="mb-3 input">
          <br>
          <label for="dateforleave" class="form-label" >Dates: </label>
          <input type="date" class="date" id="dateforleave" placeholder="YY-MM-DD" v-model="EmpDate">
          
          
        </div>
        <br>
        <div class="mb-3 input">
          <label for="typeleave" class="form-label" placeholder="">Reason: </label>
          <input type="text" class="form-control" id="typeleave" placeholder="" v-model="EmpReason" >
          <br>

          <div v-if="error.length" class="alert alert-danger">
        
          <p v-for="(e,index) in error" :key="index">{{ e }}</p>
        
      </div>
          
        </div>
        
       <button type="submit" class="btn btn-primary">Submit</button>
       <button type="button" class="mybtn" @click="handleLogout">Log out</button>
</form>
</div>


</template>

<script>
    

    export default{
       data(){
        return{
          EmpName : '',
          EmpDate : '',
          EmpReason : '',
          error : []
          
        }
        },
        methods: {
          handleSubmit(){
            this.error = [];

            if (!this.EmpName){
              this.error.push ('Please fill out employee number field!') 
            }
            if (!this.EmpDate) {
              this.error.push ('Please fill out a date!')
            }
            if (!this.EmpReason) {
              this.error.push ('Please provide reason!')
            }
            if (this.error.length === 0) {
              alert ('Form submitted successfully! Thank you.');
              
              this.EmpName = '';
              this.EmpDate = '';
              this.EmpReason = '';
            }
          },
          handleLogout(){
            alert('You have been logged out.');

            this.EmpName = '';
            this.EmpDate = '';
            this.EmpReason = '';
            this.error = [];

            this.$router.push('/')
          }
        }
        
    }


  
</script>
    

<style>
.section{
  height: 700px;
 
  z-index: 999;
  padding: 1rem;
  text-align: center;
  font-size: 1rem;

}
form{
  border: 2px solid black;
  border-radius: 30px; 
  max-width: 400px;
  margin: 50px ;
  margin-left: 35%;
  border: 2px solid black;
  border-radius: 20px; ;
  padding: 30px;
  background-color: white;

}
button{
  color: green;
  border-radius: 5px;
  font-size: large;
  padding: 4px 15px;
  margin-top: 20px;

}




input{
  width: 125px;
  height: 23px;
  border-radius: 5px;
  font-size: medium;
  
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: beige;
  margin: 0;
  padding: 0;
  text-align: center;
}  
p{
  color: red;
}

    
  </style>