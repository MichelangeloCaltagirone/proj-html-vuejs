<script>
    export default {
        data() {
            return {

            }
        },
        props: {
            picPath: {
                type: String,
                required: true
            },
            price: {
                type: String,
                required: true
            },
            name: {
                type: String,
                required: true
            },
            students: {
                type: Number,
                required: true
            },
            lessons: {
                type: Number,
                required: true
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

    <div class="card mb-3" style="max-width: 540px;">
        
        <div class="row g-0">
            <div class="col-md-4 d-flex p-3">
                <img :src="getImageUrl(picPath)" class="img-fluid rounded-circle" :alt='picPath'>
            </div>
            <div class="col-md-8">
                <div class="card-body">
                    <h5 class="card-title">{{ price }}</h5>
                    <p class="card-text"> {{ name }}</p>
                    <span class="card-text me-4"><small class="text-body-secondary"><i class="fa-solid fa-book"></i> {{ lessons }} lessons</small></span>
                    <span class="card-text"><small class="text-body-secondary"><i class="fa-regular fa-user"></i> {{ students }} students</small></span>
                </div>
            </div>
        </div>
    </div>
</div>    

</template>

<style scoped>
.card {
    background-color:  #F5F7FA;
    border: none;

    .card-title {
        color: #20AD96
    }
    .card-text:hover {
        color: #20AD96;
    }

    &:hover {
        background-color: white;
        /* box-shadow: 15px black; */
    }
}
img {
    /* border-radius: 50%; */
}
</style>