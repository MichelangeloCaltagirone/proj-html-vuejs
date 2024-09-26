<script>
export default {
  data() {
    return {
        showVideo: false,
        cover: true,
        isVideoPlaying: false,
    }
  },
  methods:{
    playVideo(){
        this.showVideo = true 
        this.cover = false
        this.isVideoPlaying = true;

        document.body.classList.add('video-playing-mode') // Classe per applicare uno sfondo nero e coprire tutti gli elementi nel body quando il video è i riproduzione
        const iframe = document.querySelector('.iframe-wrapper') 
        iframe.classList.add('iframe-extend') // aggiungo la classe per estendere l'iframe una volta cliccato
    },
    hideVideo(){
        this.showVideo = false
        this.cover = true

        document.body.classList.remove('video-playing-mode')
        const iframe = document.querySelector('.iframe-wrapper') 
        iframe.classList.remove('iframe-extend') // aggiungo la classe per rimuovere l'iframe una volta cliccato          
    },
  },
}
</script>

<template>
    <!-- Contenitore sezione iframe -->
     <section id="section-iframe-wrapper" class="d-flex">
        <div class="left">
            <!-- Contenitore per iframe video-->
            <div class="iframe-wrapper">
                <!-- Contenitore per gestire effetti ed animazione su immagine di cover e di bottone YT -->
                <div class="overlay">
                    <img id="cover-image" v-if="cover" @click="playVideo" src="https://maxcoach-4437.kxcdn.com/main/wp-content/uploads/sites/1/2019/12/home-2-popup-video-poster.jpg" alt="">
                    <div class="yt-button" v-if="cover" @click="playVideo">
                        <img src="https://maxcoach-4437.kxcdn.com/main/wp-content/uploads/sites/1/2019/11/icon-youtube-play.png" alt="">
                    </div>
                </div>
                <!-- Iframe per mostrare il video youtube con metodi e animazioni-->
                <iframe v-if="showVideo" @mouseleave="hideVideo"
                width="670" 
                height="450" 
                src="https://www.youtube.com/embed/ElFJ1qcl74U?autoplay=1" 
                frameborder="0" 
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                allowfullscreen>
                </iframe>
            </div>
        </div>
        <div class="right-page">
            <!-- Testo parte destra della sezione -->
             <div class="section-iframe-right">
               <h3 id="right-preTitle">
                   Get started <mark>effortlessly</mark>
               </h3>
               <div id="right-title-wrapper">
                   <div class="title">
                       <h2>Enjoy Our <mark>Companionship</mark> </h2>
                   </div>
               </div>
               <div class="right-page-bottom-wrapper">
                   <div id="right-description-wrapper d-flex justify-content-center">
                       <div class="text">
                           <p>Sneek peek into what has in store for you on our online teaching and mentoring portal. Seek for some hidden hints of early-bird rewards as well.</p>
                       </div>
                   </div>
                   <div id="right-link-wrapper" class="w-100 d-flex justify-content-start">
                       <a href="#">
                           <p>Download free guidebook</p>
                       </a>
                   </div>
                 </div>
            </div> 
            </div>
     </section>
</template>

<style lang="scss" scoped>
@use '../assets/styles/general.scss';
// IFRAME 
.iframe-wrapper{
    flex-basis: 50%;
    height: 450px;
    width: 670px;
    overflow: hidden; //Aggiungo l'overflow in modo che venga impedito all'immgaine di espandersi oltre il contneitore al suo hover
    position: relative;   
}

.iframe-extend{
    height: 475px;
    width: 845px;
}

iframe, img{
    width: 100%;
}

.yt-button{
    cursor: pointer;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    pointer-events: auto;
}

// IMG
#cover-image, .overlay{
    border-radius: 5px;
    transition: transform 1s ease; // Aggiungo una animazione smooth di durata 0.5s
}

.overlay:hover{
    transform: scale(1.1); // zommo l'immagine rispetto alla sua proporzione originale di 1.1 all'hover
}

.close-button {
    position: absolute;
    top: 20px;
    right: 20px;
    font-size: 2rem;
    color: white;
    cursor: pointer;}

// SECTION IFRAME RIGHT PAGE
.right-page{
    display: flex;
    justify-content: center;
    margin-left: 100px;
    text-align: left;
}

mark{
    background-color: transparent;
    margin: 0;
    padding: 0;
}

.section-iframe-right #right-preTitle{
    margin-top: 50px;
    margin-bottom: 20px;
    font-size: 15px;
    text-transform: uppercase;
    letter-spacing: 2px;
    color: #8C89A2;
} 

.section-iframe-right mark{
    font-weight: 700;
    color: #3F3A64;
}

#right-title-wrapper .title h2{
    font-family: 'Poppins', sans-serif;
    font-weight: 600;
    font-size: 48px;
    color: #3F3A64;
}

#right-title-wrapper .title mark{
    font-weight: 400;
    color: rgb(83, 170, 150);
    text-decoration: none;
}

#right-description-wrapper .text{
    font-size: 18px;
    text-align: left;
}

.text p{
    font-family: 'Roboto';
    margin-top: 25px;
    margin-bottom: 58px;
    color: rgb(116, 116, 116);
}

#right-link-wrapper a p{
    padding-bottom: 1px;
    font-weight: 700;
    color: rgb(83, 170, 150);
    border-bottom: 1px solid rgb(83, 170, 150);
    width: fit-content;
}

#right-link-wrapper a p:hover{
    cursor: pointer;
    color: rgb(135, 207, 190);
}

#right-link-wrapper a p:active{
    color: rgb(83, 170, 150);
}

// BODY 
.video-playing-mode{
    background-color: #222;
    z-index: 1001;
}
</style>
<!-- MADE BY ANDREA GULLI -->