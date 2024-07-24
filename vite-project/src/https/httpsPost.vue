<template>
    <div>
<!-- <button @click="getPosts()">Load Post</button> -->
<div v-for="post in posts" :key="post.id">
    <h3>{{post.id}}.{{post.title}}</h3>
    <h3>{{post.body}}</h3>
</div>
    </div>
</template>

<script>
import axios from 'axios'
    export default {
        name:'PostList',
           created(){
            this.getPosts();
        },
           data(){
            return{
        posts: [],
        errormsg:""
            }
        },
        methods:{
            getPosts(){
         axios.get('https://jsonplaceholder.typicode.com/posts')
         .then( (res)=> {
             this.posts= res.data;
console.log(res.data)
         })
         .catch(error => this.errormsg = error)       
            }
    }
    }
</script>

<style lang="scss" scoped>

</style>