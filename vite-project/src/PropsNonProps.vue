<template>
    <div>
<h2>Article component</h2>
<h2 v-bind="$attrs">{{title}}</h2>
<h2>Likes: {{likes}}</h2>
<h2>{{isPublished}}</h2>
    </div>
</template>

<script>
    export default {
        name: "Article",
        props:{
            title: {
                type : String,
                required: true,
                default: 'Article default title'
            },
            likes: Number,
            isPublished: Boolean,
        },
            inheritAttrs : false,
    }
</script>

<style lang="scss" scoped>

</style>