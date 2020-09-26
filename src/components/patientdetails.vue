<template>
<div><h3 class="text-center">Patients</h3></div>
  <p></p>
  
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarTogglerDemo01" aria-controls="navbarTogglerDemo01" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    
    <div class="collapse navbar-collapse" id="navbarTogglerDemo01">
      
      <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
        <router-link  to="/addpatient"><button class="btn btn-default btn-sm" id="add"> +Add New Patient</button></router-link>
        <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</div>
        <div></div>
        <button type="button" class="btn btn-default btn-sm" onclick="document.location='logout.php'" id="ExtoEx">
					<span  aria-hidden="true"></span> Export to Excel
				</button>
      </ul>
      <form class="form-inline my-2 my-lg-0">
        <input class="form-control mr-sm-2" type="search" placeholder="Filter by Patient Name      " aria-label="Search">
        
      </form>
    </div>
  </nav>
  <div class="container mt-4" id="app">
    <table class="table table-hover">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">Name &#9660;</th>
          <th scope="col">Email</th>
          <th scope="col">Phone</th>
          <th scope="col">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th>
          <th scope="col">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="patient in patients" :key="patient.id">
          <td >{{patient.sr}}</td>
          <td>{{patient.name}}</td>
          <td>{{patient.email}}</td>
          <td>{{patient.phone}}</td>
          <td><button type="button" class="btn btn-light" id="a">Edit Profile</button></td>
          <td><button type="button" class="btn btn-light" id="a">Prescription</button></td>
        </tr>
      </tbody>
    </table>
  </div>
  <div class="pagination" id="page">

    
    <a  class="active" href="#">1</a>
    <a  href="#">2</a>
    <a href="#">3</a>
    <a href="#">4</a>
    <a href="#">5</a>
    <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</p>
    <router-view/>
  </div>
  </template>
  <script>
  export default{
   name:"patientdetails",
   data(){
     return {
       patients: []
      };
    },
    created(){
          fetch("http://localhost:3000/patients")
                .then(response => {
                      return response.json();
                })
                .then(data => {
                     this.patients = data;
                });
    }
};
</script>