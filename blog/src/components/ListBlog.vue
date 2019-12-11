<template>
    <ul>
        <Post> </Post>
        <Post> </Post>
    </ul>
</template>

<script>
    import Post from "@/components/Post";
    export default {
        name: "ListBlog",
        components: {
            Post
        }
    }
</script>

<style scoped>
    ul {
        list-style-type: none;
        margin-top: 20px;
        padding: 0;
    }
</style>