<template >
    <form>
        <h2>REQUEST FOR LEAVE</h2>
        <br>

  <div class="mb-3">
    <label for="exampleInputEmail1" class="form-label">Employee number: </label>
    <input type="email" class="form-control" id="inputEmail " aria-describedby="emailHelp">
    
  </div>
  <div class="mb-3">
    <br>
    <label for="exampleInputPassword1" class="form-label" placeholder="">Password:</label>
    <input type="password" class="form-control" id="inputPassword">
    
</div>
    <br>
    <div class="mb-3">
    <label for="typeleave" class="form-label" placeholder="">Type of leave: </label>
    <input type="text" class="form-control" id="typeleave">
    </div>
  <br><br>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>

    </template>
    

<style>
section{
    display: grid;
    grid-template-columns: repeat(3,1fr);
}

    
</style>