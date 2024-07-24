<template>
    <div>
        <h2 v-if="num ===0">{{num}} The number is  </h2>
        <h2 v-else-if="num<0">Negative</h2>
<h2 v-else>{{num}} The number is  </h2>
<h2 v-show="showElement">Using v-show</h2>
<h2 v-if="showElement">Using v-if</h2>
    </div>
</template>

<script>
    export default {
        name:"ConditionalRendering",
        data() {
            return {
                num:-5,
                showElement: false
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>