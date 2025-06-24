<template >
  <div class="section">
    <form>
        <h2>REQUEST FOR LEAVE</h2>
        <br>

  <div class="mb-3 input" >
    <label for="employeeNum" class="form-label">Employee number: </label>
    <input type="text" class="form-control" id="employeeNum" aria-describedby="">
    
  </div>
  <div class="mb-3 input">
    <br>
    <label for="dateforleave" class="form-label" >Dates: </label>
    <input type="date" class="date" id="dateforleave" placeholder="YY-MM-DD">
    
    
</div>
    <br>
    <div class="mb-3 input">
    <label for="typeleave" class="form-label" placeholder="">Reason: </label>
    <input type="text" class="form-control" id="typeleave" placeholder="">
    <br><br>
      
    </div>
  <br>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
</div>

</template>

<script>
    

    export default{
      
    }
  
</script>
    

<style>
.section{
  height: 700px;
  background-color:red ;
  z-index: 999;
  padding: 1rem;
  text-align: center;
  font-size: 1rem;

}
form{
  border: 2px solid black;
  border-radius: 30px; 
  min-width: 40%;
  margin-left: 100%;


}
input{
  width: 30%;
}



    
  </style>