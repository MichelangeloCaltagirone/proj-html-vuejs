<script>

export default {
    data() {
        return {
            programBenefits: [
                {
                    picPath: 'home-2-image-box-01.png',
                    title: 'Costumize Preference',
                    text: 'Learners are given the right to arrange and customize their study schedule and timetable based on preferences.',
                    url: '',
                    btnText: 'Start here'
                },
                {
                    picPath: 'home-2-image-box-03.png',
                    title: 'Cloud Storage',
                    text: 'You can store online lessons via online cloud or download to your device and revise lessons on the way.',
                    url: '',
                    btnText: 'Get Free Quote'
                },
                {
                    picPath: 'home-2-image-box-01.png',
                    title: 'Multimedia Channels',
                    text: 'We provide study materials with various formats: video, audio, slides, doc, prints, books and applications, and more',
                    url: '',
                    btnText: 'Start here'
                }
            ]
        }
    },
    methods: {
        getImageUrl(picPath) {
            return new URL(`../assets/images/${picPath}`, import.meta.url).href
        }
    }
}
</script>

<template>



    <div class="container px-3 mb-4">

        <h5 class="text-center mt-5">MAXCOACH AVAILABLE COURSES</h5> 
        <h1 class="text-center mb-5">Access <span>Smart Tutoring</span> Program For Benefits.</h1>

        <div class="d-flex flex-wrap justify-content-lg-between row-cols-1 row-cols-md-3">
            <div v-for="(feautere, index) in programBenefits" class="card">

                <img :src="getImageUrl(feautere.picPath)" class="card-img-top img-fluid" :alt="feautere.picPath">
                <div class="card-body">
                    <h5 class="card-title mt-2">{{ feautere.title }}</h5>
                    <p class="card-text">{{ feautere.text }}</p>
                    <a href="#" class="btn grow-link">{{ feautere.btnText }}<i class="ms-2 fa-solid fa-arrow-right-long"></i></a>
                </div>
            </div>
        </div>

    </div>


</template>


<style scoped>
.card {
    border: none;

    img {
        height: 150px;
        width: 170px;
    }
}

.text-center span {
    color: #20AD96
}

.card-body a {
    padding-left: 0;
    color: #8C89A2;
    position: relative;

    &:hover {
        color: #20AD96;
    }
}
h5 {
    color: #8C89A2;
}
@media screen and (max-width: 767px) {
    .card img {
        max-width: 150px;
        max-height: 130px;
    }
}
 /* Linea verde sotto al link, che si riempie gradualmente  */
.card .grow-link::before {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 1px;
  background-color: #28a745;
  transition: width 0.5s ease;
}

/* La linea si riempie quando si fa hover */
.card .grow-link:hover::before {
  width: 100%;
}
</style>