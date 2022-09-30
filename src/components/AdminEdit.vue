<template>
    <div style="float:left;justify-content: start;">
        <div>
            <h2>Add new blog post</h2>
            heading: <input v-model="heading">
            text: <input v-model="text">
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
            date:Date.now()
        }
    },
    mounted(){

    },
    methods:{

    }
}
</script>
