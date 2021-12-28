<template>
    <div class="body">
        <div id="banner" class="hero">
            <img src="../assets/images/planeSelfie.png" id="thumbnail"> 
            <h1 id="title">Gitup &amp; Go Travel Blog</h1>
            <h2 id="subtitle">"...may all your travels be with me"</h2>
            <img src="../assets/images/airplaneDark.png" class =" plane topPlane" id="topPlane" title="hovering cartoon airplane">
        </div>

        <v-row justify="end ma-4">
            <v-menu
                bottom
                origin="center center"
                transition="scale-transition"
            >
                <template v-slot:activator="{ on, attrs }">
                <v-btn
                    class="ml-100 pa-md-4 mx-lg-r"
                    color="white green--text"
                    dark
                    v-bind="attrs"
                    v-on="on"
                >
                    Jump down to our past adventures!
                </v-btn>
                
                </template>
        
                <v-list>
                <v-list-item
                    v-for="(item, i) in items"
                    :key="i"
                >
                    <a :href="'#' + item.id">
                    <v-list-item-title  v-html="item.title">{{ item.title }}</v-list-item-title>
                    </a>
                    </v-list-item>  
                </v-list>
            </v-menu>
        </v-row>

        <aside class="signup">
            <label for="inputs">want email updates?</label>
            <input class="inputs" id="firstName" v-model="firstname" value="first name" onfocus="this.value=''" >
            <input class="inputs" id="lastName" v-model="lastname" value="last name" onfocus="this.value=''" >
            <label for="email">email</label>
            <input type="email" class="inputs" id="email" v-model="email" value="email" onfocus="this.value=''" required>
            <button class="inputs" id="send" value="send" v-on:click="SignUps">send</button>
        </aside>

        <div class="blogEntry">
            <div class="blogBox" id="dec2021box">
                <h3 class="blogPlace" >Hometown Coeur d'Alene</h3>
                <h4 class="blogDate">Dec15-31,2021</h4>
                <div class="pContainer">
                    <p id="de2021text"><strong>Sam and Olivia both worked out some time with the folks</strong> right here in good old Coeur d'Alene. We spent some of the time working remotely and patiently sharing wi-fi. But we also managed to find time to eat out together, go on walks, shovel snow, and take in the new Cda on Ice skating rink downtown. Sam and Olivia get extra points for knowing how to skate backwards and Doug and Kristin get points for being the oldest couple on the rink. </p>
                </div>
            </div>
            <div class="pictures success" id="dec2021">
                <v-carousel class="carousel">
                    <v-carousel-item>
                        <img src="../assets/dec2021images/woodFamSkating.jpg" title="the Wood Family Skating">
                        <img src="../assets/dec2021images/woodFamCloseup.jpg" title="Wood Family Closeup">
                        <img src="../assets/dec2021images/KristinSamOlivia.jpg" title="Kristin, Sam, and Olivia">
                    </v-carousel-item>
                    <v-carousel-item>
                        <img src="../assets/dec2021images/mom&daughter.jpg" title="Kristin and Olivia">
                        <img src="../assets/dec2021images/mom&daughter2.jpg" title="Two girls skating">
                        <video class="accent" autoplay muted controls>
                            <source src="../assets/dec2021images/Cda on Ice Skating.mp4" type="video/mp4">
                            <source src="movie.ogg" type="video/ogg">
                            Your browser does not support the video tag.
                        </video>
                    </v-carousel-item>
                    <v-carousel-item
                        transition="fade-transition">
                        <img src="../assets/dec2021images/Sam.jpg" title="brother Sam">
                        <img src="../assets/dec2021images/D&K.jpg" title="Doug and Kristin">
                    </v-carousel-item>
                    <v-carousel-item>
                        <img src="../assets/dec2021images/resortfam.jpg" title="Wood family at the cda resort">
                        <img src="../assets/dec2021images/xmasfam.jpg" title="Wood family downtown">
                        <img src="../assets/dec2021images/xmasD&K.jpg" title="Doug and Kristin downtown">
                    </v-carousel-item>
                    <v-carousel-item>
                        <img src="../assets/dec2021images/5000views.jpg" title="Checkin in on TikTok!">
                    </v-carousel-item>
                </v-carousel>   
             </div>
        </div>
        <div class="blogEntry">
            <div class="blogBox" id="nov2021box">
                <img src="../assets/images/airplaneDark.png" class="plane blogPlane" title="cartoon airplane">
                <h3 class="blogPlace">Sunny San Diego, CA</h3>
                <h4 class="blogDate"> Nov 20-25,2021</h4>
                <div class="pContainer">
                    <p id="nov2021text"><strong>Once again,we hopped on an Alaska Air 737-800</strong> and made a quick non-stop trip to our home-away-from-home...sunny San Diego. Kaylee and Kyle had offered several months ago to host our family dinner at their new place. It made sense since Sam had just freshly relocated to the same area and Olivia was in transition back from a month in Hawaii. We stayed just a block down Honeycutt street from the Lachmanns. We had a great meal, enjoyed some walks and bike rides, and as an added bonus were honored with the presence of Michael and Kaitlyn (Squanda) Reimer, who generously agreed to join us for thanksgiving day. That morning, before our turkey dinner, some of us headed out to Tremaline beach and surfed. As we all headed home in the following hours, we agreed to make this a tradition! </p>
                </div>
            </div>
            <div class="pictures success" id="nov2021">
                <v-carousel class="carousel">
                    <v-carousel-item>
                    <img src="../assets/images/Honeycutt Condo.jpg" title="the Honeycutt condo">
                    <img src="../assets/images/condoVW.jpg" title="some beachhouse artwork">
                    <img src="../assets/images/eyeingTheSurf.jpg" title="Michael and Kaitlyn in the surf">
                    </v-carousel-item>
                    <v-carousel-item
                    transition="fade-transition"
                    >
                    <img src="../assets/images/honeycuttJeep.jpg" title="a vintage jeep">
                    <img src="../assets/images/KaitlynsNewBoard.jpg" title="Kaitlyn and her new board">
                    <img src="../assets/images/phoebe.jpg" title="Pheobe the cat">
                    </v-carousel-item>
                    <v-carousel-item>
                    <img src="../assets/images/surferLivCopy.png" title="surfer Olivia">
                    <img src="../assets/images/samOnTheBeach copy.jpg" title="Sam on the beach">
                    <img src="../assets/images/Cards@theHoneycutt.png" title="playing cards in the condo">
                    </v-carousel-item>
                    <v-carousel-item
                        transition="fade-transition">
                    <img src="../assets/images/toesInTheSand.jpg" title="toes in the sand">
                    <img src="../assets/images/sanDiegoPier.jpg" title="The San Diego Pier">
                    </v-carousel-item>
                </v-carousel>
             </div>
        </div>
        <div class="subscribers">email list:
            {{emailList}}
        </div>
       
     </div>

</template>

<script>

    export default {
        data() {
            return {
                message: "",
                firstname: "first name",
                lastname: "last name",
                email: "email",
                emailList: ["Joe", "Shmo", "joe@gmail.com"],
                items: [
                    { 
                    title: '...Belize Jan 2022',
                    id: "nov2021box" 
                    },
                    { 
                    title: '...San Diego March 2022 Spring Break',
                    id: "nov2021box" 
                    },
                    { 
                    title: "Hometown Coeur d'Alene 2021", 
                    id: "dec2021box"
                    },
                    { 
                    title: 'San Diego Nov 2021',
                    id: "nov2021box" 
                    },
                    { 
                    title: 'Summer 2021',
                    id: "nov2021box" 
                    },
                    { 
                    title: 'Spring 2021',
                    id: "nov2021box" 
                    },
                    ],
                    }
                },

                methods: {
                    SignUps: function(firstname) {
                        this.emailList.push(this.firstname,this.lastname,this.email);            
                        },
                
            }
        }

</script>


<!-- styling section -->
<style scoped>



    @import url('https://fonts.googleapis.com/css2?family=Comforter+Brush&family=Raleway:ital,wght@0,200;1,100&display=swap');
    * {
    display: flexbox;
    }

    .body{
        height: auto;
        background-color: black;

    }

    div {
        color:greenyellow;
        height: auto;
    }


    h1 {
        font-size: 4rem;
        font-family: 'Raleway', sans-serif;
        color:greenyellow;
        margin: 1rem 0 0 0;
        z-index: 10;

    }

    h2 {
        font-size: 2rem;    
        font-family: 'Comforter Brush', cursive;    
        color:greenyellow;
        margin: 1rem 0 0 0;
        z-index: 10;

    }

    #thumbnail {
        height: 80px;
        padding: 0;
        /* margin: 10% 0 0 20%; */
    }

    #topPlane{
        height: 180px;
        width: auto;
        margin: 0 0 0 800px;
        z-index: 0;
        transition: all linear 1.5s
    }

    #topPlane:hover {
        margin: -400px 0 0 1000px;
    }

    .plane {
        height: 180px;
        width: auto;
    }

    .blogPlane{
        position: fixed;
        margin: -40px 0 0 840px;
        z-index: 2;
    }

    #banner {
        display: flexbox;
        padding: 2rem;
        width: 100%;
        height: 100px;
        text-align: center;
        justify-content: center;
        justify-items: center;
        background-color: rgb(49, 85, 85);
        align-items: center;
        /* border: solid red 10px; */
    }

#title {
    width: 100%;
}

    #subtitle{
        width: 100%;
    } 

    aside {
        font-size: 1rem;
        /* color: whitesmoke;
        border: solid greenyellow; */
        width: 250px;
        height: auto;
        text-align: start;
        margin: 0 0 8px 25px;
    }

    .aside label {
        width: 100%;
    }

    label{
        margin: 0 0 0 8px;
    }

    .inputs{
        font-size: 1rem;
        color:khaki;
        border-style: solid;
        border-color: greenyellow;
        padding: 3px;
        margin: 2px;
        width: 100%;

    }
    #send {
        border-radius: 4px;
        padding: 3px;
        margin: 3px;
        box-shadow: 3px 3px 3px;
        width: 50px;
    }

    #send:active{
        background-color: chartreuse;
    }

    nav {
        position:absolute;
        display: inline-block;
        margin: -7% 0 0 45%;
        /* border: solid red 5px;  */
    }

   

    p {
        color: white;
        font-family: 'Raleway', sans-serif;
        font-size: 16px;
        width: 75%;
        margin: 2% 0 5% 5%;
    }


    .blogBox{
        position: relative;
    }

    .blogEntry {
        display: flexbox;
        height: auto;
        width: 90%;
        border: solid blue 5px;
        border-radius: 3px;
        margin: 0 5% 5% 2%;
        z-index: 1;
    }

    .pContainer{
        text-align: justify;
        /* border: solid red 5px; */
    }

    .pictures { 
        display: flex;
        margin: 0px 2% 2% 2%;
        padding: 0 2% 2% 2%;
        overflow:auto;
        border: solid red 5px;

    }
    /* .carousel{
        height: 2200px;
    } */

    .pictures{
        height: 500px;
        width: auto;
        padding: 5px;
    }

   img{
        /* display: flexbox; */
        /* max-height: 300px; */
        height: 420px;
        width: auto;
        padding: 5px;
        }

    video {
        width: 400px; 
        height: 495px;
             }

    #nov2021text {
        /* width: 400px; */
        color: white;
                /* border: solid red 5px; */
    }

    .blogBox {
        overflow:scroll;
        /* border: solid red 5px; */
        margin: 5%;
    }

    .subscribers{
        width: 100%;
        border: solid red 5px;
    }

    @media only screen and (max-width: 1250px) {   
         #banner{
            width: 1200px;
         }
            h1{
                color: red;
            }
            aside{
                width: 175px;
            }
    }

    @media only screen and (max-width: 500px) {  
    
        
        #banner{
            height: 50px;
        } 
        #title { 
            font-size: 16px;
            margin:0px;
            }
        #subtitle {
            font-size: 8px;
            margin: -5px 0 0 0;
            }
        .signup {
            margin: 40px 0 0 5px;
            font-size: 10px;
            width: 25%
        }

        .inputs,#firstName,#lastName {
            font-size: 10px;
            
        }
        #thumbnail{
            height: 50px;
            margin: -10px 0 0 0;
        }   
        nav{
            font-size: 12px;
        }
        .pContainer {
            height: 20  0px;
        }

        p {
            font-size: 8px;
        }
    }

        video {
            border: solid blue 5px;

        }
        
    

</style>