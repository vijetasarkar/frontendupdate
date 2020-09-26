<template>
<div><nav class="navbar fixed-top navbar-light bg-light" id="topnav">
    <a class="navbar-brand" id="head" >EZ MEDS</a>
   <router-link to="/"> <button type="button" class="btn btn-default btn-sm"  id="log">
      <span  aria-hidden="true"></span> Logout
    </button></router-link>
  </nav></div>
  <p><br></p>
 <router-link to="/patientdetails">Login</router-link>
  <router-view/>

  </template>
  <script>
  export default{
    name:"app"
  }
  </script>
  <style scoped>
  #head
{
    color: white;
    font-weight: 700;
}
#topnav
{
    background-color: #44474B !important;
}
#log
{
    background-color: white;
    padding-top:0px;
    padding-bottom:0px;
    padding-right:15px;
    padding-left:15px;
    font-weight: 550;
    float:right;
}
#log:hover
{
    background-color:#007FFF;
    color: white;
    font-weight:2em ;
    padding-top:2px;
    padding-bottom:2px;
    padding-right:20px;
    padding-left:20px;
    
    
}
</style>

