<template>
    <div>
   List Rendering
   <h2 v-for="(name, index) in names" :key="index"> {{index}} {{name}}</h2>
   <h2 v-for="name in fullNames" :key="name.first">{{name.first}}-{{name.last}}</h2>
   <div v-for='actor in actors' :key="actor">
       <h2>{{actor.name}}</h2>
<h2 v-for="movie in actor.movies" :key="movie">{{movie}}
</h2> 
   </div>
    </div>
</template>

<script>
    export default {
        name:"ListRendering",
        data() {
            return {
               names: ['Bruce','Clark','Diana'],
               fullNames: [
                   {first: 'Bruce1',last:'Wane1'},
                    {first: 'Bruce2',last:'Wane2'},
                     {first: 'Bruce3',last:'Wane3'}
               ],
               actors:[
                   {
name:'actor1',
movies:['Batman','This Princess']
                   },
                   {
name:'actor2',
movies:['Batman2','This Princess2']
                   },
                   {
name:'actor3',
movies:['Batman3','This Princess3']
                   },
               ] 
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>