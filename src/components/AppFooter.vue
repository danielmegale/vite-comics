<script>
    export default{
        data(){
            return{
                icons:[
                    {
                        icon:'footer-facebook.png'
                    },
                    {
                        icon:'footer-periscope.png'
                    },
                    {
                        icon:'footer-pinterest.png'
                    },
                    {
                        icon:'footer-twitter.png'
                    },
                    {
                        icon:'footer-youtube.png'
                    }
                ]
            }
        },
        methods:{
        getIcon(target){
                const url=new URL(`../assets/img/${target}`,import.meta.url)  
                return url.href
            }
        }

    }
</script>


<template>
    <div>
        <main>
            <div class="container">
                <div class="ul-flex">
                    <div>
                        <ul>DC COMICS
                            <li>Characters</li>
                            <li>Comics</li>
                            <li>Movies</li>
                            <li>TV</li>
                            <li>Games</li>
                            <li>Videos</li>
                            <li>News</li>
                        </ul>
                        <ul>SHOP
                            <li>Shop DC</li>
                            <li>Shop DC Collactibles</li>
                        </ul>
                    </div>
                    <ul>DC
                        <li>Terms of Use</li>
                        <li>Privacy plicy(New)</li>
                        <li>Ad Choices</li>
                        <li>Advertising</li>
                        <li>Jobs</li>
                        <li>Subscriptions</li>
                        <li>Talent Workshops</li>
                        <li>CPSC Certificates</li>
                        <li>Ratings</li>
                        <li>Shop Help</li>
                        <li>Contacts Us</li>
                    </ul>
                    <ul>SITES
                        <li>DC</li>
                        <li>MAD magazine</li>
                        <li>DC Kids</li>
                        <li>DC Universe</li>
                        <li>Dc Power Visa</li>
                    </ul>
                </div>
            </div>
            
        </main>
        <footer>
            <div class="container f-flex">
                <button>SING-UP NOW</button>
                <div class="flex">
                    <div v-for="icon in icons">
                        <img :src="getIcon(icon.icon)" alt="">
                </div>
                </div>
            </div>
        </footer>
    </div>
</template>


<style lang="scss" scoped>
main{
    height: 660px;
    background-image:url(../assets/img/dc-logo-bg.png),url(../assets/img/footer-bg.jpg);
    background-position-x:75%;
    background-position-y:50% ;
    background-repeat: no-repeat;
    background-size:30%,cover;
}
footer{
    height: 110px;
    background-color: #303030;
}
button{
    padding: 10px;
    background-color: #303030;
    border: 2px solid #0282F9;
    color: #fff;
    font-weight:500;
    font-size: 20px;
}
.ul-flex{
    display: flex;
    gap: 30px;
    color: #fff;
    padding: 50px 0;
}
.f-flex{
    display: flex;
    align-items: center;
    height: 100%;
    justify-content: space-between;
}
.flex{
    display: flex;
}
ul{
    font-size: 30px;
    font-weight: 600;
}
li{
    color: gray;
    font-size: 15px;
}
</style>