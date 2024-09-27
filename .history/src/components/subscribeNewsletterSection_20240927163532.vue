<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <section class="py-5 my-5 w-75 m-auto">

        <div class="container">

            <div class="row row-cols-1 align-items-center d-flex justify-content-center align-items-center">

                <div class="col text-center">

                    <div class="fw-bold fs-1 my-5">Subscribe <span class="c-green fw-medium">Newsletters</span></div>
                    <p class="c-grey fs-3 text-wrap mb-5 fw-semibold">Enter your email address to register to our
                        newsletter
                        subscription
                        delivered on a regular basis!</p>
                </div>

                <div class="col">

                    <div class="input-group mb-3">
                        <div class="form-floating c-grey text-center email-bar">
                            <input type="email" class="form-control bg-grey border border-0 h" id="SubscribeNewsletter"
                                placeholder="Enter your email">
                            <label for="SubscribeNewsletter">Enter your email</label>
                        </div>
                        <button class="btn btn-lg input-group-text bg-green text-light fs-4">Confirm identity</button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.eamil-bar {
    height: 80px;
}

.c-green {
    color: #20AD96;
}

.c-grey {
    color: #696969;
}

.bg-green {
    background-color: #20AD96;
}

.bg-grey {
    background-color: #F8F8F8;
}
</style>