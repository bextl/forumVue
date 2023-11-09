<template>
    <div class="app">
        <post-form/>
        <post-list :posts = "posts"/>
        
            
        
       

    </div>
</template>

<script>
import PostForm from "./components/PostForm"
import PostList from "./components/PostList"


export default{
    components: {
        PostList, PostForm
    }, 

    data(){
        return{
        posts: [
            {id: 1, title: 'Javascript', body: 'Description of the post'},
            {id: 2, title: 'Javascript 2', body: 'Description of the post 2 '},
            {id: 3, title: 'Javascript 3', body: 'Description of the post 3'},
            {id: 4, title: 'Javascript 4', body: 'Description of the post 4'},
        ],
        title: '',
        body: '',
        
    }
}, 
methods: {
    createPost(){
        const newPost = {
            id: Date.now(),
            title: this.title,
            body: this.body,
        }
        this.posts.push(newPost);
        this.title = '';
        this.body = '';

    },
    // inputTitle(event) {
       
    //     this.title = event.target.value;

    // }

},

}

</script>

<style>

</style>

