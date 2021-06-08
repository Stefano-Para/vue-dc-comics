<template>
  <header>

      <div id="container_header">
          
        <img src="../assets/dc-logo.png" alt="">
        <ul>
            <li v-for="(link, index) in links" :key="index">
                <a
                :href="link.url"
                :class="{ active: link.current }">
                    {{ link.text }}
                </a>
            </li>
        </ul>

      </div>      

  </header>
</template>

<script>
export default {
   name: 'Header',
   data: function () {
       return {
           links: [
                {
                    text: "Characters",
                    url: "#Characters",
                    current: false
                },
                {
                    text: "Comics",
                    url: "#Comics",
                    current: true
                },
                {
                    text: "Movies",
                    url: "#Movies",
                    current: false
                },
                {
                    text: "TV",
                    url: "#TV",
                    current: false
                },
                {
                    text: "Games",
                    url: "#Games",
                    current: false
                },
                {
                    text: "Collectibles",
                    url: "#Collectibles",
                    current: false
                },
                {
                    text: "Videos",
                    url: "#Videos",
                    current: false
                },
                {
                    text: "Fans",
                    url: "#Fans",
                    current: false
                },
                {
                    text: "News",
                    url: "#News",
                    current: false
                },
                {
                    text: "Shop",
                    url: "#Shop",
                    current: false
                },
               
           ]
       }
   }
}
</script>

<style lang="scss" scoped>
    #container_header {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        width: 80%;
        margin: 0 auto;
        height: 80px;
    }
    img {
        width: 50px;
    }
    ul {
        display: flex;
        list-style-type: none;
    }
    a {
        padding: 10px 10px 28px;
        color: black;
        font-size: 12px;
        font-weight: 600;
        text-decoration: none;
        list-style: none;
        text-transform: uppercase;
    }
    a.active,
    a:hover {
        border-bottom: 4px solid  #0282f9;
        color: #0282f9;
    }
</style>