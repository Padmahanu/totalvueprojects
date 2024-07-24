<template>
    <div>
App
<CreatePost/>
    </div>
</template>

<script>
import axios from 'axios'
import CreatePost from './https/CreatePost.vue'
    export default {
        name:"httcalls",
        components:{
CreatePost
        }
     
        
    }
</script>

<style lang="scss" scoped>

</style>