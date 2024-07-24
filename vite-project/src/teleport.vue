<template>

App
<teleport to="#portal-root">
<Portal/>
</teleport>
   
</template>

<script>
import Portal from './Components/Portal.vue'
    export default {
        name: "teleport",
components:{
    Portal
}
    }
</script>

<style lang="scss" scoped>

</style>