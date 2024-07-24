<template>
    <div>
<input type="text"  ref="inputRef">
<PostList ref="postRef"/>
    </div>
</template>

<script>
import PostList from '../src/https/httpsPost.vue'
    export default {
        name:'TemplateRef',
        components:{
            PostList
        },
        mounted(){ 
            console.log(this.$refs.postRef)
            this.$refs.inpuRef.focus()
        }
    }
</script>

<style lang="scss" scoped>

</style>