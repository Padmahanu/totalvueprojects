<template>
    <div>
App
<h2 v-once> {{name}}</h2>

<button @click="name = 'hanu'">Change Name</button>
<h2 v-pre>{{name}}</h2>
    </div>
</template>

<script>
    export default {
        name:'modifier',
        data(){
            return{
name:'padma'
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>