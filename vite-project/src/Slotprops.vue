<template>
   
<NameList>
    <template v-slot:default="slotProps">
    FullName:    {{slotProps.f}} {{slotProps.l}}
    </template>
</NameList>
  <NameList>
    <template v-slot:default="slotProps">
    FirstName:    {{slotProps.f}}
    </template>
</NameList>
  <NameList>
    <template v-slot:default="slotProps">
     LastName:   {{slotProps.l}}
    </template>
</NameList>
</template>

<script>
import NameList from './Components/NameList.vue'
    export default {
        name:"slotprops",
          components:{
          NameList
      }, 
       data(){
            return{
            
            }
        },
        methods:{
    
        }
    }
</script>

<style lang="scss" scoped>

</style>