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
    <input type="text" class="text" id="dateforleave" placeholder="YY-MM-DD">
    
    
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
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: lightslategray;
  text-align: center;
}


form {
  background-color: lightblue;
  max-width: 400px;
  margin: 50px auto;
  padding: 30px;
  border-radius: 15px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  border: 2px solid #d0e7ff;
}

h2 {
  color: darkblue;
  margin-bottom: 20px;
}

label {
  display: block;
  margin: 15px 0 5px;
  color: black;
  font-weight: 500;
  text-align: left;
}

input[type="text"],
input[type="date"],
select {
  width: 100%;
  padding: 10px;
  border: 1px solid #aacbee;
  border-radius: 8px;
  box-sizing: border-box;
  font-size: 14px;
}

input[type="submit"] {
  margin-top: 20px;
  padding: 10px 25px;
  background-color: #0d6efd;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  font-weight: bold;
}

input[type="submit"]:hover {
  background-color: #0a58ca;
  
}
button{
  color: green ; 
 
}


    
  </style>