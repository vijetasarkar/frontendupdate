<template>

<form   id="add-patient">
        
        
          <div class="login-box ">
            <h5 >Add Patient</h5>
          
          <div class="col-md-8 login" >
            <label  >First Name&nbsp;&nbsp;&nbsp;</label>
            <input type="text" id="a" >
          </div>
          <div class="col-md-8  login" >
            <label >Last Name&nbsp;&nbsp;&nbsp;</label>
            <input type="text" id="a"  >
          </div>
          <div class="col-md-8 login" >
            <label >Email&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
            <input type="email" id="a" >
          </div>
          <div class="col-md-8 login">
            <label >Phone&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
            <input type="tel" id="a" >
          </div>

          <div  class="col-md-8 login">
            <button  class="btn btn-vue ">Cancel  </button>
             <button  class="btn btn-primary  ">Save</button>
          </div>
          
        
        </div>
      </form>
      </template>

    <script>
      
      export default{
          name: 'addpatient',
      }
       
    </script>

    <style scoped >
    .btn-vue
{
    background:#A9A9A9;
    color:#fff;
    font-weight: bold;

}
.btn-vue:hover
{
  background-color:blue ;
  color: #fff;
  
}


  
  #add-patient
  {
    
    width: 50%;
    margin:auto 0;
    
  
    
    align-content: center !important;
    text-align: center;
  }
    

  

.login-box{
  max-width: 200px; 
  float: none;
  margin: 100px auto;
  margin-right:100px;

  top: 50%;
  left: 50%;
}


.login{
  background:#DCDCDC;
  padding: 15px;
  display: inline !important;
  text-align: center;
  width:200px;
  
}


#a
{
  text-align: center;
  border-radius: 5px;
  border-width: 1px;
}


    </style>