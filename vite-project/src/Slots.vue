<template>
    <div>
App  
<Card>Card Content</Card>
<Card>
    <h1>Card Content</h1>
</Card>
<Card>
   <img src="https://picsum.photos/200" alt="">
</Card>
<Card>
    <template v-slot:header>
     <h3>Header</h3>
    </template>
    <template v-slot:default>
       <img src="https://picsum.photos/200" alt="">
    </template>
    <template v-slot:footer>
       <button>View Details</button>
    </template>
</Card>
<NameList/>
    </div>
</template>

<script>
import Card from './Components/CardSlots.vue'


    export default {
        name: 'App',
      components:{
          Card
      },
        data(){
            return{
            
            }
        },
        methods:{
    
        }
    }
</script>

<style scoped>

</style>