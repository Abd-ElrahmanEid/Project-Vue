<template>
    <div class="box">
            <h2>{{ content }}</h2>
    </div>
    <br>
</template>



<script>

    export default{
        name: 'item_box',
        props: ['content']
    }

</script>




<style>
    *{
        padding: 0;
        margin: 0;
        box-sizing: border-box;
    }
    .box{
        width: 50%;
        height: 80px;
        border: 2px solid black;
        text-align: center;
        background-color: black;
        margin: auto;
    }

    h2{
        color: white;
        padding-top: 15px;
    }

</style>