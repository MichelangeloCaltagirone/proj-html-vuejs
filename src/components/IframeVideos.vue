<script>
export default {
  data() {
    return {
        showVideo: false,
        cover: true,
    }
  },
  methods:{
    playVideo(){
        this.showVideo = true 
        this.cover = false
        const iframe = document.querySelector('.iframe-wrapper') 
        iframe.classList.add('iframe-extend') // aggiungo la classe per estendere l'iframe una volta cliccato
        document.body.classList.add('bg-black')
    },
    hideVideo(){
        this.showVideo = false
        this.cover = true
        const iframe = document.querySelector('.iframe-wrapper') 
        document.body.classList.remove('bg-black')
        iframe.classList.remove('iframe-extend') // aggiungo la classe per rimuovere l'iframe una volta cliccato        
    },
  },
}
</script>

<template>
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
</template>

<style lang="scss" scoped>
// IFRAME 
.iframe-wrapper{
    height: 450px;
    width: 100%;
    overflow: hidden; //Aggiungo l'overlow in modo che venga impedito all'immgaine di espandersi oltre il contneitore al suo hover
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
</style>

<!-- MADE BY ANDREA GULLI -->