<template>
    <form @submit.prevent>
            <h4>Создание поста</h4>
            <input v-model='post.title' class="input" type="text" placeholder="Название">
            <input v-model='post.body' class="input" type="text" placeholder="Описание">
            <button class="btn" @click="create_post">Создать пост</button>
    </form>
</template>

<script>
export default {
    data() {
        return {
            post: {
                title: '',
                body: ''
            }
        }
    },
    methods: {
        create_post(){
                this.id = Date.now();
                this.$emit('create', this.post);
                this.post={
                    title : '',
                    body : '',
                }
        }
    }
}
</script>

<style lang="css" scoped>
form {
    display: flex;
    flex-direction: column;
    justify-content: center;
}
.input {
    width:100%;
    border: 2 solid teal;
    margin-top: 15px;
    padding: 10px 15px;
}
.btn {
    margin-top: 15px;
    align-self: flex-end;
    padding: 10px 15px;
}
</style>