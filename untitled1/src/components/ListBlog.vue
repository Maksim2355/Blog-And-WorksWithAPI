<template>
    <ul>
        <Post
                v-bind:REG="REG_FLAG"
        />
    </ul>
</template>

<script>
    import Post from "@/components/Post";
    export default {
        name: "ListBlog",
        props: ['REG_FLAG'],
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