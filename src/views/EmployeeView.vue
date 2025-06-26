<template >
  <div class="section">
    <form @submit.prevent="handleSubmit">
        <h2>LEAVE REQUEST</h2>
        <br>
        
        <div class="mb-3 input" >
          <label for="employeeNum" class="form-label">Employee name: </label>
          <input type="text" class="form-control" id="employeeName" aria-describedby="" v-model="EmpName" required>
          
        </div>
        <div class="mb-3 input">
          <br>
          <label for="dateforleave" class="form-label" >Dates: </label>
          <input  type="date" class="date" id="dateforleave" placeholder="YY-MM-DD" v-model="EmpDate" required>
          
          
        </div>
        <br>
        <div class="mb-3 input">
          <label for="typeleave" class="form-label" placeholder="">Reason: </label>
          <select v-model="EmpReason" required>
            <option disabled value="">Please select a reason</option>
            <option>Sick Leave</option>
            <option>Personal</option>
            <option>Family Responsibilty</option>
            <option>Vacation</option>
            <option>Medical Appointment</option>
            <option>Bereavement</option>
            <option>ChildCare</option>
            <option>Other</option>
          </select>
          <br>

          
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
          
          
        };
        },
        methods: {
          handleLogout(){
            alert('You have been logged out.');

            this.EmpName = '';
            this.EmpDate = '';
            this.EmpReason = '';
            

            this.$router.push('/')
          },
          handleSubmit(){
            alert('Form submitted successfully! Thank you.')

            this.EmpName = '';
            this.EmpDate = '';
            this.EmpReason = '';

          }
         

         

        },

        
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