<template>
    <div style="float:left;justify-content: start;">
        <div>
            <h2>Add new blog post</h2>
            heading: <input v-model="heading">
            text: <input v-model="text">
            <button @click="newBlogPost">Add</button>

        </div>
        <br>
        <div>
            <h2>Add new Event</h2>
            name: <input v-model="name">
            description: <input v-model="description">
            date: <input v-model="date">
        </div>
        <br>

        <div>
            <h2>Add new Lesson</h2>
            name: <input v-model="subject">
            start: <input v-model="start">
            end: <input v-model="end">
        
        </div>
        <br>

    </div>
    
</template>
<script>

export default {
    name:"adminEdit",
    data(){
        return{
            date:Date.now(),
            heading:"",
            text:"",
            name:"",
            description:"",
            subject:"",
            start:"",
            end:""
        }
    },
    mounted(){

    },
    methods:{
        newBlogPost(){
            const requestOptions = {
            method: "POST",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify({ blogpost:{
                    heading: this.heading,
                    text:this.text,
                    postedAt:this.date
                }
}           )
            };
                fetch("http://127.0.0.1:8000/api/blogpost/store", requestOptions)
            .then(response => response.json())
            .then(data => (this.postId = data.id));
}
        }
    }
</script>
