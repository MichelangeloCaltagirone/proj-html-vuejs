<script>

    export default {
        data() {
            return {
                programBenefits: [
                    {
                        picPath: 'home-2-image-box-01.png',
                        title: 'Costumize Preference',
                        text: 'Learners are given the right to arrange and customize their study schedule and timetable based on preferences.',
                        url: ''
                    },
                    {
                        picPath: 'home-2-image-box-03.png',
                        title: 'Cloud Storage',
                        text: 'You can store online lessons via online cloud or download to your device and revise lessons on the way.',
                        url: ''
                    },
                    {
                        picPath: 'home-2-image-box-01.png',
                        title: 'Multimedia Channels',
                        text: 'We provide study materials with various formats: video, audio, slides, doc, prints, books and applications.',
                        url: ''
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

    <div class="container">

        <h5 class="text-center">MAXCOACH AVAILABLE COURSES</h5>
        <h1 class="text-center mb-5">Access Smart Tutoring Program For Benefits.</h1>

        <div class="d-flex justify-content-between">
        <div v-for="(feautere, index) in programBenefits" class="card" style="width: 18rem;">

            <img :src="getImageUrl(feautere.picPath)" class="card-img-top" :alt="feautere.picPath">
            <div class="card-body">
                <h5 class="card-title">{{ feautere.title }}</h5>
                <p class="card-text">{{ feautere.text }}</p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
        </div>
    </div>

    </div>
    
    
</template>

<style scoped>
</style>