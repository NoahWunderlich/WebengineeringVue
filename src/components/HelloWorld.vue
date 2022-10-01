<template>
  <div>
    <iframe style="float:left;max-width: 300px; border: none; min-height: 260px; background-color: transparent;" src="https://www.wetter.de/widget/heute/u1wxws/false/"></iframe><br/><a href="https://www.wetter.de" rel="nofollow" target="_blank"></a>
    <div style="width:40%;float:left">
      <h2>Blogposts</h2>
      <br>
      <br>
      <div v-for="(item, index) in blogData" :key = index>
      <h3>{{item.heading}}</h3>
      <br>
      <h5>{{item.postedAt.split('T')[0]}}</h5>
      <br>
      <a>{{item.text}}</a>
      <br>
    <br>
      </div>
    </div>

    <div style="width:40%;float:right">
      <h2>Upcoming Events</h2>
      <br>
      <br>
      <div v-for="(item, index) in eventData" :key = index>
      <h3>{{item.name}}</h3>
      <br>
      <h5>Beginning at: {{item.start.slice(0, -3).replace('T',' ')}}</h5>
      <br>
      <a>{{item.description}}</a>
      <br>
    <br>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',

  data(){
    return{
      eventData:[],
      blogData:[]
    }
  },
  mounted() {
    this.getData();
  },
  methods:{
    async getData(){
        const eventResponse = await fetch("http://127.0.0.1:8000/api/events");
        this.eventData = await eventResponse.json();
        console.log(this.eventData);

        const blogResponse = await fetch("http://127.0.0.1:8000/api/blogposts");
        this.blogData = await blogResponse.json();
        console.log(this.blogData);
    }
  }
}
</script>

<style>

</style>
