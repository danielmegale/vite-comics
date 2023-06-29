<script>
    export default{
        data(){
            return{
                links:[
                    {
                        text: 'Characters',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'Comics',
                        url: '#',
                        current: true,
                    },
                    {
                        text: 'Movies',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'TV',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'Games',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'Collectibles',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'Videos',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'Fans',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'News',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'Shop',
                        url: '#',
                        current: false,
                    },
                ]
            }
        }
    }   
</script>
<template>
    <header>
        <nav>
            <img src="../assets/img/dc-logo.png" alt="">
            <ul>
                <li v-for="link in links" :key="link.text" :class="{active: link.current}"><a :href="link.url">{{link.text}}</a></li>
            </ul>
        </nav>
    </header>
</template>
<style lang="scss" scoped>
nav{
    display: flex;
    justify-content: space-between;
    height: 70px;
    background-color: #fff;
};
ul{
    display: flex;
    gap: 15px;
    align-items: center;
    li{
        a{
            text-decoration: none;
            color: #000;
            padding: 17.5px 0;
            &:hover{
                color: #0282F9;
                border-bottom: 5px solid #0282F9;
            };
            &:active{
                background-color: #0282F9;
                color: #000
            }
        };
    };
};
</style>