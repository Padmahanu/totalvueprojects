<template>
    <div>
<form @submit.prevent="handleclick">
    <div>
        <label for="userId">Post userid</label>
        <input type="text" id="userId" v-model="formdata.userId"><br/>
                <label for="title">Post title</label>
        <input type="text" id="title" v-model="formdata.title"><br/>
                <label for="body">Post body</label>
        <input type="text" id="body" v-model="formdata.body"><br/>
        <button>Submit</button>
    </div>
</form>
    </div>
</template>

<script>
import axios from 'axios'
    export default {
        name:'CreatePost',
     
        data(){
            return{
                formdata:{
                    userId:'',
                    title:'',
                    body:''
                }
            }
        },
        methods:{
            handleclick(){
axios.post('https://jsonplaceholder.typicode.com/posts',this.formdata)
.then( res => console.log(res))
.catch( err => console.log(err))
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>