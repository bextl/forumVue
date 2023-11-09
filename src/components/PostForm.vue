
<template>
<form @submit.prevent>
    <h3>Creating a post</h3>
    <input 
    v-bind:value="post.title" 
    @input="post.title = $event.target.value"
    class="input" 
    type="text" 
    placeholder="name">

    <input 
    v-bind:value="post.body"
    @input="post.body = $event.target.value"
    class="input" 
    type="text"
     placeholder="description">

    <button class="btn">Ad d Post</button>
</form>


</template>


<script>
export default{
    data(){
        return {
            post: {
                title: '',
                body: '',
            }
        }
    }
}


</script>


<style>
*{
    margin: 0;
    padding: 0;
    box-sizing: 0;
}

form{
    display: flex;
    flex-direction: column;
}
.input{
    width: 100%;
    border: 1px solid teal;
    padding: 10px 15px; 
    margin-top: 15px;
}
.btn{
    align-self: flex-end;
    margin-top: 15px;
    padding: 10px 15px;
    background: none;
    color: teal;
    border: 1px solid teal;
}

.app{
    padding: 20px;
}


</style>