<template>
    <div>
<h2>Option -{{ofirst}} last =>{{olast}} middle =>{{ohero}}</h2>
<h2>Composition -{{cfirst}}</h2>
<h2>Composition greet-{{greet}}</h2>
<h2>Composition cgreet-{{cgreet}}</h2>
<h2>Composition {{state.ofirst}} {{state.olast}} {{state.ohero}}</h2>
    </div>
</template>

<script>
import {ref,reactive} from 'vue'
    export default {
        name:'Data',
        setup(){
 const cfirst = ref('Clark')
  const clast = ref('kent')
   const cmiddle = ref('Superman')
 cfirst.value='Diana'
 const greet =`Hello ${cfirst.value}`
 const cgreet =`Hello ${cfirst.value} ${clast.value} ${cmiddle.value}`
 console.log(cfirst,"cfirst")
 const state =reactive({
  ofirst : 'Padma',
                olast : 'hanu',
                ohero : 'surya'
 })

 const reactiveHero =`Hello ${state.ofirst} ${state.olast} ${state.ohero}`
 return {
     cfirst,
     greet,
     cgreet,
     state,
     reactiveHero
 }
        },
        data(){
            return{
                ofirst : 'Padma',
                olast : 'hanu',
                ohero : 'surya'
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>