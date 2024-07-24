<template>
    <div>
<h2>Counter {{value}}</h2>
<button @click="incrementdata">CLick increment {{counter}}</button>
<h2 @mouseover="incrementdata"> Hover increment {{counter}}</h2>
    </div>
</template>

<script>
import counter from '../src/mixins/counter'
   export default{
       name: 'Mixins',
       data(){
           return{
value:'Padma'
           }
       },
       mixins:[counter]
   }
</script>

<style lang="scss" scoped>

</style>