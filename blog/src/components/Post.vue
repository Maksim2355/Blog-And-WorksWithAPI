<template>
    <div class="flex-container" >
        <h2>{{post.title}}</h2>
        <hr>
        <li>
            <a>
                {{post.content}}
            </a>
        </li>
        <button type="submit"
                v-if="REG"
                v-on:click="$emit('edit-post', post.id)"
        >Редактировать</button>
    </div>
</template>

<script>
    export default {
        name: "Post",
        props: {
            REG: {
                type: Boolean,
                required: true
            },
            post: {
                type: Object,
                required: true
            }
        }

    }
</script>



<style scoped>
    .flex-container {
        display: flex;
        flex-direction: column;
        border: 2px solid #2c3e50;
        padding: .001rem 2rem;
        background: #A3D0C3;
        margin-top: 20px;

    }

    a {
        font-size: 17px;
    }

    li {
        justify-content: space-between;
        margin-bottom: 1rem;
        font-size: 16px;

    }
    button {
        display: inline-block;
        font-family: arial,sans-serif;
        font-size: 15px;
        font-weight: bold;
        color: rgb(68,68,68);
        text-decoration: none;
        user-select: none;
        padding: .2em 1.2em;
        outline: none;
        border: 1px solid rgba(0,0,0,.1);
        border-radius: 2px;
        background: beige;
        transition: all .218s ease 0s;
    }
    button:hover {
        color: rgb(24,24,24);
        border: 1px solid rgb(198,198,198);
        background: #f7f7f7 linear-gradient(#f7f7f7, #f1f1f1);
        box-shadow: 0 1px 2px rgba(0,0,0,.1);
    }
    button:active {
        color: rgb(51,51,51);
        border: 1px solid rgb(204,204,204);
        background: rgb(238,238,238) linear-gradient(rgb(238,238,238), rgb(224,224,224));
        box-shadow: 0 1px 2px rgba(0,0,0,.1) inset;
    }

</style>