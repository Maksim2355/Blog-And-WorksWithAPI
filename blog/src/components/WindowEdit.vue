<template>
<div class="flex">
    <div class="b-popup">
        <div class="b-popup-content">
            <button>Zakroi</button>
            <textarea>РЕДАЧИМ</textarea>
        </div>
    </div>
</div>
</template>

<script>
    export default {
        name: "WindowEdit"
    }
</script>

<style scoped>
    *{
        font-family: Areal;
    }

    textarea{
        width: 99.4%;
        height: 85%;
        font-family: 'Merriweather', serif;
    }
    .b-popup{
        width:100%;
        min-height:100%;
        background-color: rgba(0,0,0,0.5);
        overflow:hidden;
        position:fixed;
        top:0px;
    }
    .b-popup .b-popup-content{
        margin:40px auto 0px auto;
        width:1000px;
        height: 400px;
        padding:10px;
        background-color: #7BA7AB;
        border-radius:3px;
        box-shadow: 0px 0px 10px #000;
    }
    .b-popup-content {
        display: flex;
        flex-direction: column;
    }

    button {
        text-align:center;
        font-size:13px;
        text-decoration: none;
        font-weight: 700;
        padding: 3px 6px;
        background: #eaeef1;
        display:block;
        width:60px;
        margin: 20px auto;
        background-image: linear-gradient(rgba(0,0,0,0), rgba(0,0,0,.1));
        border-radius: 3px;
        color: rgba(0,0,0,.6);
        text-shadow: 0 1px 1px rgba(255,255,255,.7);
        box-shadow: 0 0 0 1px rgba(0,0,0,.2), 0 1px 2px rgba(0,0,0,.2), inset 0 1px 2px rgba(255,255,255,.7);
    }

    button:hover, button.hover {
        background: #fff;
    }
    button:active, button.active {
        background: #d0d3d6;
        background-image: linear-gradient(rgba(0,0,0,.1), rgba(0,0,0,0));
        box-shadow: inset 0 0 2px rgba(0,0,0,.2), inset 0 2px 5px rgba(0,0,0,.2), 0 1px rgba(255,255,255,.2);
    }
</style>