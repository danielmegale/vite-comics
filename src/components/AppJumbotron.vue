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
                        image:'buy-comics-digital-comics.png',
                        text:'DC MERCHANDISE'
                    },
                    {
                        image:'buy-comics-digital-comics.png',
                        text:'SUBSCRIPTION'
                    },
                    {
                        image:'buy-comics-digital-comics.png',
                        text:'COMIC SHOP LOCATOR'
                    },
                    {
                        image:'buy-comics-digital-comics.png',
                        text:'DC POWER VISA'
                    },
                ],
            }
        },
        methods:{
        getImage(image){
                const url=new url(`../assets/img/${images.image}`,import.meta.url)  
                console.log(url)
            }
        }
    }
</script>


<template>
    <figure>
        <div v-for="image in images">
            <img :src="getImage(image)" alt="">
            <p></p>
        </div>
    </figure>
</template>


<style lang="scss" scoped>
    figure{
        background-color:#0282F9;
        height: 108px;
    }
</style>