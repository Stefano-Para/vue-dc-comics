<template>
  <footer>

      <div id="container_columns">

            <div class="column left">
                <div class="small_columns">
                    <h3>Dc Comics</h3>
                    <ul>
                        <li>                            
                            <a href="">
                                Characters
                            </a>
                        </li>
                        <li>
                            <a href="">
                                Comics
                            </a>
                        </li>
                        <li>
                            <a href="">
                                Movies
                            </a>
                        </li>
                        <li>
                            <a href="">
                                TV  
                            </a>
                        </li>
                        <li>
                            <a href="">
                                Games
                            </a>
                        </li>
                        <li>
                            <a href="">
                                Videos
                            </a>
                        </li>
                        <li>
                            <a href="">
                                News
                            </a>
                        </li>
                    </ul>
                </div> <!-- small column  -->
                
                <div class="small_columns">
                    <h3>DC</h3>
                    <ul>
                        <li>
                            <a href="">
                                Terms Of Use
                            </a>
                        </li>
                        <li>
                            <a href="">
                                Privacy policy (New)
                            </a>
                        </li>
                        <li>
                            <a href="">
                                Ad Choices
                            </a>
                        </li>
                        <li>
                            <a href="">
                                Advertising
                            </a>
                        </li>
                        <li>
                            <a href="">
                                Jobs
                            </a>
                        </li>
                        <li>
                            <a href="">
                                Subscriptions
                            </a>
                        </li>
                        <li>
                            <a href="">
                                Talent Workshops
                            </a>
                        </li>
                        <li>
                            <a href="">
                                CPSC Certificates
                            </a>
                        </li>
                        <li>
                            <a href="">
                                Rating
                            </a>
                        </li>
                        <li>
                            <a href="">
                                Shop Help
                            </a>
                        </li>
                        <li>
                            <a href="">
                                Contact Us
                            </a>
                        </li>
                    </ul>
                </div> <!-- small column  -->

                <div class="small_columns">
                    <h3>Sites</h3>
                    <li>
                        <a href="">
                            DC
                        </a>
                    </li>
                    <li>
                        <a href="">
                            MAD Magazine
                        </a>
                    </li>
                    <li>
                        <a href="">
                            DC Kids
                        </a>
                    </li>
                    <li>
                        <a href="">
                            DC Universe
                        </a>
                    </li>
                    <li>
                        <a href="">
                            DC Power Visa
                        </a>
                    </li>                    
                </div> <!-- small column  -->
                <div class="small_columns">
                    <h3>Shop</h3>
                    <li>
                        <a href="">
                            Shop DC
                        </a>
                    </li>
                    <li>
                        <a href="">
                            Shop DC Collectibles
                        </a>
                    </li>
                </div>
            </div>
            <div class="column right">
                <img src="../assets/dc-logo-bg.png" alt="">
            </div>
      </div>
      <div class="last-section">
          <div class="container_80">
              <div class="sign_in_button">
                  <a href="#Sign-In">Sign Up now!</a>
              </div>
              <div class="follow_us">
                  
                  <ul>
                      <li><h5>Follow us</h5></li>
                      <li v-for="(follow, index) in follows" :key="index">
                          <a href="">
                              <img :src="follow.img" :alt="follow.url">
                          </a>
                      </li>
                  </ul>
              </div>
          </div>
      </div>
      
  </footer>
</template>

<script>
export default {
    name: 'Footer',
    data: function () {
        return {
            follows: [
                {
                    name: "Facebook",
                    url: "#facebookDC",
                    img: require('../assets/footer-facebook.png')
                },
                {
                    name: "Twitter",
                    url: "#twitterDC",
                    img: require('../assets/footer-twitter.png')
                },
                {
                    name: "Twitter",
                    url: "#yutubeDC",
                    img: require('../assets/footer-youtube.png')
                },
                {
                    name: "Twitter",
                    url: "#pinterestDC",
                    img: require('../assets/footer-pinterest.png')
                },
                {
                    name: "Twitter",
                    url: "#periscopeDC",
                    img: require('../assets/footer-periscope.png')
                },

            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    footer {
        // height: 300px;
        background: url("../assets/footer-bg.jpg");
        background-repeat: no-repeat;
        background-size: cover;
    }
    #container_columns {
        display: flex;
        width: 80%;
        margin: 0 auto;
        color: white;
    }
    .column {
        width: 50%;
    }
    .left {
        display: flex;
        padding-top: 15px; 
    }
    .right {
        height: 300px;
        position: relative;
    }
    .right img {
        width: 60%;
        position: absolute;
        bottom: -40px;
        overflow: hidden;
        z-index: 1;
    }
    .small_columns {
        margin: 10px 10px 10px 0px;   
    }
    .small_columns li {
        list-style: none;
        opacity: 0.5;
        // margin: -2px 0;
    }
    a {
        font-size: 10px;
        text-decoration: none;
        color: white;
    }
    .last-section {
        margin: 0 auto;
        position: relative;
        background-color: #303030;
        height: 100px;
        z-index: 2;
    }
    .container_80 {
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 80%;
        margin: 0 auto;
    }
    .sign_in_button a {
        text-transform: uppercase;
        font-size: 18px;
        border: 2px solid #0282f9;
        padding: 10px;
            :hover {
            background-color: #0282f9;
            border: 2px solid blue;
            }
    }
    .sign_in_button 
    .follow_us {
        color: white;
    }
    .follow_us img {
        width: 20px;
        height: 20px;
    }
    .follow_us ul {
        display: flex;
        flex-direction: row;
        align-items: center;
        // list-style-type: none;
    }
    .follow_us li {
        margin: 0 4px;
        text-decoration: none;
        list-style: none;
    }
    li h5 {
        color: #0282f9;
        text-transform: uppercase;
        font-size: 20px;
        margin-right: 15px;
    }
</style>