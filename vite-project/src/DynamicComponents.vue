<template>
    <div>
<button @click="activetab= 'TabA'">TabA</button>
<button @click="activetab= 'TabB'">TabB</button>
<button @click="activetab= 'TabC'">TabC</button>
<keep-alive>
<component :is="activetab"/>
</keep-alive>
<!-- <TabA v-if="activetab === 'TabA'"/>
<TabB v-if="activetab === 'TabB'"/>
<TabC v-if="activetab === 'TabC'"/> -->

    </div>
</template>

<script>
import TabA from './dynamiccon/TabA.vue'
import TabB from './dynamiccon/TabB.vue'
import TabC from './dynamiccon/TabC.vue'

    export default {
        name:"App",
        components:{
            TabA,TabB,TabC
        },
        data(){
            return{
                activetab: 'TabA'
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>