<template>
 
<h2>Hi {{this.name}}  age: {{age}}
    </h2>

</template>

<script>
    export default {
        name:'ComponentBasic',
        props: ['name','age']
    }
</script>

<style lang="scss" scoped>

</style>