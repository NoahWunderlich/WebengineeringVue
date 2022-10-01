<template>
    <div >
      <div >
        <div v-for="(item, index) in data" :key = index>
      </div>
      <div class="weekdays">
        <h2>Monday</h2>

      </div>
      <div class="weekdays"> 
        <h2>Tuesday</h2>

    </div>
    <div class="weekdays"> 
        <h2>Wednesday</h2>

    </div>
    <div class="weekdays"> 
        <h2>Thursday</h2>

    </div>
    <div class="weekdays"> 
        <h2>Friday</h2>

    </div>

      </div>
  
    </div>
  </template>
  <script>
  export default{
      name:"TimeTable",
      data(){
          return {
          data : null
          }
  
      },
      mounted(){
          this.loadData();
      },
      methods:{
          async loadData(){
              const response = await fetch("http://127.0.0.1:8000/api/items");
              this.data = await response.json();
              console.log(this.data[0].subject);
              console.log(this.data[1]);
  
          }
      }
  }
  </script>
  <style>
.weekdays{
    margin:8px;
    background-color: lightgray;
    float:left;
    width:15%;
    height:400px;
}
  </style>