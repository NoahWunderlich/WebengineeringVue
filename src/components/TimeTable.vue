<template>
    <div>
      <h1>This is an timetable page</h1>
  
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
  