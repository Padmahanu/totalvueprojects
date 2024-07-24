<template>
  <h3 v-for="name in names" :key="name.f">
     <slot :f="name.f" :l="name.l"></slot>
  </h3>
</template>

<script>
    export default {
        name: "NameList",
        data(){
            return{
                names:[
                    {
                        f:'padma1',
                        l:"n1"
                    },
                     {
                        f:'padma2',
                        l:"n2"
                    },
                     {
                        f:'padma3',
                        l:"n3"
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>