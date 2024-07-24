<template>
    <div>
<h2>Volume Tracker (0-20) </h2>
    <h2> Current : {{volume}}</h2>
<button @click="volume += 2">Increment</button>
<button @click="volume -= 2">Decrement</button>
    </div>
    <input type="text" v-model="movie"> Movie
        <input type="text" v-model="movieInfor.title"> 
            <input type="text" v-model="movieInfor.actor"> 
            <button @click="movielist=movielist.concat('Padma')">Add List</button>
            <h2>{{movielist}}</h2>
</template>

<script>
import ComponentBasic from './ComponentBasics.vue'
    export default {
        name: "Watchers",
        components:{
            ComponentBasic,
        },
        data(){
            return{
                volume: 0,
                movie:'Batman',
                movieInfor :{
                    title:'',
                    actor:''
                },
                movielist:[
                    'Batman', 'Superman'
                ]
            }
        },
        methods:{

        },
        computed:{

        },
        watch:{
                volume(newValue, oldValue)
                {
                newValue === 16 && newValue > oldValue ? alert('Danger'):''
                },

                movie: {
                    handler(newValue){
                    console.log(`call api movie name =${newValue}`) 
                    },
                    immediate : true
                },
                movieInfor:{
                    handler(newValue){
                console.log(`Calling API with ${newValue.title} and actor is ${newValue.actor}`)
                    },
                    deep : true
                },
                movielist:{
                    handler(newValue){
 console.log(`updated list ${newValue}`)
                    }
                }
                }
                }
    
</script>

<style lang="scss" scoped>

</style>