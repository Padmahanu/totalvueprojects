<template>
    <div>
        <h4>App Component</h4>
<ChildStyles>
    <h4>Child Styles Component</h4>
    </ChildStyles>
    </div>
</template>

<script>
import ChildStyles from './ChildStyles.vue'
    export default {
        name:'StyleApp',
        components:{
            ChildStyles
        }
    }
</script>

<style scoped>
h4{
    color: #000;
}
</style>