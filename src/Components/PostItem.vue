<template>
    <div class="post">
        <div>Название: {{post.title}}</div>
        <div>Описание: {{post.body}}</div>
    </div>
</template>

<script>
    export default {
        props:{
            post:{
                type: Object,
                required: true,
            },
        }
    }
</script>

<style lang="css" scoped>
.post {
    margin-top: 15px;
    padding: 15px;
    border: 2px solid teal;
}
</style>