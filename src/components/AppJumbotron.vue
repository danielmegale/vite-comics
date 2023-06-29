<script>
    export default{
        data(){
            return{
                images:[
                    {
                        image:'buy-comics-digital-comics.png',
                        text:'DIGITAL COMICS'
                    },
                    {
                        image:'buy-comics-merchandise.png',
                        text:'DC MERCHANDISE'
                    },
                    {
                        image:'buy-comics-shop-locator.png',
                        text:'SUBSCRIPTION'
                    },
                    {
                        image:'buy-comics-subscriptions.png',
                        text:'COMIC SHOP LOCATOR'
                    },
                    {
                        image:'buy-dc-power-visa.svg',
                        text:'DC POWER VISA'
                    },
                ],
            }
        },
        methods:{
        getImage(target){
                const url=new URL(`../assets/img/${target}`,import.meta.url)  
                return url.href
            }
        }
    }
</script>


<template>
    <div class="height">
        <figure class="container">
            <div class="row" v-for="image in images">
                <img :src="getImage(image.image)" alt="">
                <p>{{image.text }}</p>
            </div>
        </figure>
    </div>
</template>


<style lang="scss" scoped>
    div{
        background-color:#0282F9;
        img{
            height: 50px;
        }
        figure{
            display: flex;
            justify-content: space-between;
        }
    }
    .row{
        display: flex;
        align-items: center;
        padding: 25px 0;
        gap:10px;
        color: #fff;
    }
    .height{
        height:200px;
    }
    figure{
        height: 100%;
    }
</style>