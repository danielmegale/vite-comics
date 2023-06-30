<script>
    export default{
        props:{
            comics:Array,
        },
    }
</script>


<template>
<main>
    <h1 class="container">Contents goes here </h1>
    <figure class="container">
        <div v-for="comic in comics">
            <div class="card-container">
                <img :src="comic.thumb" :key="comic.series" :alt="comic.series">
            </div>
            <figcaption>{{comic.series}}</figcaption>
        </div>
    </figure>
</main>
</template>


<style lang="scss" scoped>
    main{
        background-color: #000;
        padding: 50px 0;
    }
    h1{
        color:#fff;
    }
    figure{
        display: flex;
        flex-wrap: wrap;
        gap: 15px;
        div{
            width: calc(100% / 6 - 15px);
            margin-bottom: 30px;
        }
        img{
            width: 100%;
            height: 257px;
            object-fit: cover;
        }
        figcaption{
            color: #fff;
        }
    }
    .card-container{
        width: 100%;
        height: 165px;
        overflow: hidden;
    }
</style>