<template>
    <div>
<h2>Component F</h2>
<h2>{{username}}</h2>
    </div>
</template>

<script>
    export default {
         name: 'ComponentF',
         inject:['username']
    }
</script>

<style lang="scss" scoped>

</style>