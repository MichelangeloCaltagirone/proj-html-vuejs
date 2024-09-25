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

    }
}
</script>

<template>

    <div class="container">
        <div class="card mb-3" style="max-width: 540px;">
            <div class="row g-0">
                <div class="col-md-4">
                    <img :src="picPath" class="img-fluid rounded-start" :alt='picPath'>
                </div>
                <div class="col-md-8">
                    <div class="card-body">
                        <h5 class="card-title">{{ price }}</h5>
                        <p class="card-text"> {{ name }}</p>
                        <p class="card-text"><small class="text-body-secondary">i {{ lessons }} lessons</small></p>
                        <p class="card-text"><small class="text-body-secondary">i {{ students }} students</small></p>

                    </div>
                </div>
            </div>
        </div>
    </div>

</template>

<style scoped></style>