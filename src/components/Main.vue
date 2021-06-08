<template>
    <main>
        <!-- black section  -->
        <div id="container_black">            
            <div id="black_section">
                <h5>--> Content goes Here!</h5>
            </div>                           
        </div> <!--  chiusura container black  -->

        <!-- blue section logos  -->
        <div id="container_blue">
            <div id="navbar">
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a href="">
                            <!-- come si fa?  -->
                            <img :src="link.img" alt="">
                            {{ link.text }} 
                        </a>
                    </li>
                </ul>
            </div>
        </div> 
    </main>
</template>

<script>
    export default {
        name: 'Main',
        data: function () {
        return {
            links: [
                    {
                        text: "Digital Comics",
                        url: "#Digital_Comics",
                        img: require('../assets/buy-comics-digital-comics.png'),
                        current: false
                    },
                    {
                        text: "Dc Merchandise",
                        url: "#Dc_Merchandise",
                        img: require('../assets/buy-comics-merchandise.png'),
                        current: true
                    },
                    {
                        text: "Subscription",
                        url: "#Subscription",
                        img: require('../assets/buy-comics-subscriptions.png'),
                        current: false
                    },
                    {
                        text: "Comic Shop locator",
                        url: "#Comic_Shop_locator",
                        img: require('../assets/buy-comics-shop-locator.png'),
                        current: false
                    },
                    {
                        text: "DC Power Visa",
                        url: "#DC_Power_Visa",
                        img: require('../assets/buy-dc-power-visa.svg'),
                        current: false
                    },
            ]
        }
   }
    }
</script>

<style scoped>
    #container_black {
        height: 80px;
        width: 100%;
        background-color: black;
    }
    #black_section {        
        margin: 0 auto;
        height: 80px;
        width: 80%;
        color: white;
        line-height: 80px;
        vertical-align: middle;
    }
    #container_blue {    
        display: flex;
        align-items: center;
        /* justify-content: space-around; */
        height: 100px;
        width: 100%;
        background-color: #0282f9;
    }
    #navbar {
        margin: 0 auto;
        width: 80%;
    }
    ul {
        display: flex;
        justify-content: space-between;
    }
    li {
        list-style: none;
    }
    a {
        color: white;
        text-decoration: none;

    }
    a img {
        width: 20px;
        height: 20px;
    }
</style>