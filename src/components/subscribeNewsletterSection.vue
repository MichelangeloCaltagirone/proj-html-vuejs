<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <section class="py-5 my-5 m-auto text-center">

        <div class="container">

            <div class="row justify-content-center align-items-center">

                <div class="col-lg-8 mb-4">
                    <h2 class="fw-bold fs-1 my-4">Subscribe to <span class="c-green fw-medium">Newsletters</span></h2>
                    <p class="c-grey fs-5">Enter your email address to register for our newsletter, delivered on a
                        regular basis!</p>
                </div>

                <div class="col-lg-5">
                    <div class="input-group input-group-lg mb-3">
                        <div class="form-floating flex-grow-1">
                            <input type="email" class="form-control bg-grey border-0" id="SubscribeNewsletter"
                                placeholder="Enter your email">
                            <label for="SubscribeNewsletter">Enter your email</label>
                        </div>
                        <button class="btn btn-lg input-group-text bg-green text-white">Subscribe</button>
                    </div>
                </div>
            </div>

        </div>

    </section>
</template>

<style lang="scss" scoped>
section {
    height: 10;
}

.c-green {
    color: #20AD96;
}

.bg-green {
    background-color: #20AD96;
}

.bg-grey {
    background-color: #F8F8F8;
}
</style>