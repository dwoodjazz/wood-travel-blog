<template>
    <div class="body">
        <div id="banner" class="hero">
            <img src="../assets/images/planeSelfie.png" id="thumbnail"> 
            <h1 id="title">Gitup &amp; Go Travel Blog</h1>
            <h2 id="subtitle">"...may all your travels be with me"</h2>
            <img src="../assets/images/airplaneDark.png" class ="plane topPlane" id="topPlane" title="hovering cartoon airplane">
        </div>
<!--  -->
        <v-row  >
            <v-menu
                bottom
                origin="center center"
                transition="scale-transition"
            >
                <template v-slot:activator="{ on, attrs }">
                    <v-btn id="jumpBtn" 
                        
                        color="white green--text"
                        font-size="5px"
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
            <label for="inputs" id="label">want email updates?</label>
            <input class="inputs" id="firstName" v-model="firstname" value="first name" onfocus="this.value=''" >
            <input class="inputs" id="lastName" v-model="lastname" value="last name" onfocus="this.value=''" >
            <label for="email" id="emailLabel">email</label>
            <input type="email" class="inputs" id="email" v-model="email" value="email" onfocus="this.value=''" required>
            <button class="inputs" id="send" value="send" v-on:click="SignUps">send</button>
        </aside>

        <div class="blogEntry">
            <div class="blogBox" id="jan2022box">
                <h3 class="blogPlace" >Ambergris Caye, Belize</h3>
                <h4 class="blogDate">Jan 15-23,2022</h4>
                <div class="pContainer">
                    <p id="de2021text"><strong>Our all-time #1 bucket-list destination came to be in celebration </strong>of our 32nd anniversary. We headed to the airport at 3am and enjoyed our business class six-hour flight to Belize City. All of the preparation and planning and covid testing paid off. It was beautiful and peaceful and the people were wonderful. We spent the week on the dock, in a golf cart, and walking the shores of San Pedro and beyond. We enjoyed our trip and did well without the creature comforts of our modern life.</p>
                </div>
            </div>
            <div class="pictures success" id="Jan2022">
                <v-carousel class="carousel">
                    <v-carousel-item class="item">
                        <img src="../assets/images/belize2022/legs.jpg" title="Kristin on the dock">
                    </v-carousel-item>
                    <v-carousel-item>
                        <video 
                            class="accent" 
                            autoplay 
                            muted 
                            controls>
                        <source src="../assets/images/belize2022/cart-in-san-pedro (1).mp4" type="video/mp4" title="cart in San Pedro">
                        </video>
                    </v-carousel-item>
                    <v-carousel-item>
                        <img src="../assets/images/belize2022/secret-sunset.jpg" title="sunset at secret beach">
                    </v-carousel-item>
                    <v-carousel-item>
                        <img src="../assets/images/belize2022/Tranquility-Bay.jpg" title="the shore at Tranquility Bay">
                    </v-carousel-item>
                    <v-carousel-item>
                        <img src="../assets/images/belize2022/spike-tail-black-iguana.jpg" title="iguana">
                    </v-carousel-item>
                    <v-carousel-item>
                        <img src="../assets/images/belize2022/sunset-family.jpg" title="a family at sunset">
                    </v-carousel-item>
                    <v-carousel-item
                        >
                        <img src="../assets/images/belize2022/secret-beach.jpg" title="Secret Beach Sign">
                    </v-carousel-item>
                    <v-carousel-item>
                        <img src="../assets/images/belize2022/secret-sunset.jpg" title="Sunset at Secret Beach">
                    </v-carousel-item>
                    <v-carousel-item>
                        <img src="../assets/images/belize2022/sunset-couple.jpg" title="us at sunset">
                    </v-carousel-item>
                    <v-carousel-item>
                        <img src="../assets/images/belize2022/steps-to-breakfast.jpg" title="the path to breakfast">
                    </v-carousel-item>
                    <v-carousel-item>
                        <img src="../assets/images/belize2022/handstand.jpg" title="a handstand at sunset">
                    </v-carousel-item>
                    <v-carousel-item>
                        <video class="accent" autoplay muted controls>
                            <source src="../assets/images/belize2022/swaying-palms.mp4" type="video/mp4">
                            <source src="movie.ogg" type="video/ogg">
                            Your browser does not support the video tag.
                        </video>
                    </v-carousel-item>
                </v-carousel>   
             </div>
        </div>
        <div class="blogEntry">
            <img src="../assets/images/airplaneDark.png" class ="plane topPlane" id="topPlane" title="hovering cartoon airplane">
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
            <img src="../assets/images/airplaneDark.png" class ="plane topPlane" id="topPlane" title="hovering cartoon airplane">
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
                    id: "jan2021box" 
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
        /* display: flexbox; */
        height: auto;
        width: 100%;
        background-color: black;

    }

    div {
        color:greenyellow;
        height: auto;
    }
        #banner {
        display: flexbox;
        padding: 2rem;
        margin: 0 0 60px 0; 
        width: 100%;
        height: 100px;
        text-align: center;
        justify-content: center;
        justify-items: center;
        background-color: rgb(49, 85, 85);
        align-items: center;
        /* border: solid red 10px; */
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
        margin: 0 0 0 60%;
        z-index: 0;
        transition: all linear 3.5s
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

    #jumpBtn {
        width: 40%;
        height: 28px;
        font-size: 18px;
        margin: 170px 0 0 28%;
    }

#title {
    width: 100%;
}

    #subtitle{
        width: 100%;
    } 

    .signup {
        font-size: 1rem;
        /* color: whitesmoke;
        border: solid greenyellow; */
        width: 250px;
        height: auto;
        text-align: start;
        margin: 0 0 18px 25px;
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
    #label,#emailLabel{
        margin-left: 20px;
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

.blogEntry {
        display: flexbox;
        height: auto;
        width: 90%;
        border: solid blue 5px;
        border-radius: 3px;
        margin: 5%   5% 5% 2%;
        z-index: 1;
    }
    .blogBox{
        position: relative;
    }

    

    .pContainer{
        text-align: justify;
        /* border: solid red 5px; */
    }

    .pictures { 
        display: flex;
        flex-direction: column;
        align-items: center;
        margin: 0px 2% 2% 2%;
        padding: 0 2% 2% 2%;
        overflow:auto;
        border: solid red 5px;

    }
   .carousel {
        display: flex;
        justify-content: center;
        align-items: center;
        overflow: hidden;
        width: 24em;
        min-height: 25em;
}

    .pictures{
        height: 500px;
        width: auto;
        padding: 5px 5px 30px 5px;
    }

   img{
        /* display: flexbox; */
        /* max-height: 300px; */
        height: 420px;
        width: auto;
        padding: 5px 5px 30px 5px;
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


/* <--Media Queries begin here---> */


    @media only screen and (max-width: 1250px) {   
         #banner{
            width: 100%;
         }
            aside{
                width: 175px;
            }
    }

    @media only screen and (max-width: 973px) {  
        #jumpBtn {
        width: 45%;
        font-size: 16px;
        margin: 160px 0 0 23%;
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
        
        @media only screen and (max-width: 410px) {  
        #banner{
            margin: 0;
            /* width: 200px; */
        }
         .signup {
            margin: 40px 0 0 5px;
            font-size: 10px;
            width: 40%
        }
        #label {
            width: 50%;
        }
      
     #jumpBtn {
        width: 60%;
        font-size: 10px;
        margin: 60px 0 0 18%;
        }
    }

</style>