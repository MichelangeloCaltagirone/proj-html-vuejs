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

    }
}
</script>

<template>

<div class="container">

    <div class="card mb-3">
        
        <div class="row py-1 g-0">
            <div class="col-4 p-lg-2">
                <img :src="getImageUrl(picPath)" class="rounded-circle" :alt='picPath'>
            </div>
            <div class="col-8">
                <div class="card-body">
                    <h5 class="card-title fs-4 fw-bold">{{ price }}</h5>
                    <p class="card-text fw-bold fs-5"> {{ name }}</p>
                    <span class="card-text me-4"><small class="text-body-secondary"><i class="fa-solid fa-book"></i> {{ lessons }} lessons</small></span>
                    <span class="card-text"><small class="text-body-secondary"><i class="ms-2 fa-regular fa-user"></i> {{ students }} students</small></span>
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
    .card-text {
        color: #3F3A64;
        &:hover {
            color: #20AD96;
        }
        
    }

    &:hover {
        background-color: white;
    }
}
img {
    width: 150px;
    height: 150px;
    object-fit: cover;
    margin-right: 1rem;
}
@media screen and (max-width: 767px) {
  img {
    width: 95px;
    height: 95px;
  }
}
@media screen and (max-width: 991px) {
    .col-4 {
        display: flex;
        align-items: center;
        justify-content: center;
    }
    
}

</style>
