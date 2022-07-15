<template>
    <div class="app">
        <!-- <div>Кол-во лайков {{likes}}</div>
        <div>Кол-во дизлайков {{dislikes}}</div>
        <div>
            <button v-on:click="addLike">like</button>
            <button @click="addDislike">dislike</button>
        </div> -->
        <post-form @create="create_post" />
        <post-list :posts="posts" />
    </div>    
</template>
<script>
import PostForm from "@/Components/PostForm";
import PostList from "@/Components/PostList";
    export default {
        components: {
            PostForm, PostList
        },
        data() {
            return {
                // likes: 0,
                // dislikes: 0,
                posts:[
                    {id:0, title: 1, body: 2},
                    {id:1, title: 2, body: 3},
                    {id:2, title: 3, body: 4},
                ],
            }
        },
        methods:{
            // addLike(){
            //     this.likes += 1;
            // },
            // addDislike(){
            //     this.dislikes += 1;
            // }
            create_post(post){
                this.posts.push(post);
            },
        },
    }
</script>
<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.app {
    padding: 20px;
}
</style>