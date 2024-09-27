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

        <div class="d-flex justify-content-between row-cols row-cols-md-3">
            <div v-for="(feautere, index) in programBenefits" class="card" style="width: 18rem;">

                <img :src="getImageUrl(feautere.picPath)" class="card-img-top img-fluid" :alt="feautere.picPath">
                <div class="card-body">
                    <h5 class="card-title mt-2">{{ feautere.title }}</h5>
                    <p class="card-text">{{ feautere.text }}</p>
                    <a href="#" class="btn">{{ feautere.btnText }}<i class="ms-2 fa-solid fa-arrow-right-long"></i></a>
                </div>
            </div>
        </div>

    </div>


</template>

<style scoped>
.card {
    border: none;

    img {
        height: 130px;
        width: 150px;
    }
}

.text-center span {
    color: #20AD96
}

.card-body a {
    padding-left: 0;
    color: #8C89A2;

    &:hover {
        color: #20AD96;
    }
}

h5 {
    color: #8C89A2;
}
</style>