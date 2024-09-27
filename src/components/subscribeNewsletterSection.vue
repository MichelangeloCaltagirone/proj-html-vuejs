<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="conatiner-fluid py-3">

        <div class="row row-cols-2 align-items-center">

            <div class="col">

                <div class="fw-bold fs-1">Subscribe <span class="c-green fw-medium">Newsletters</span></div>
                <p class="c-grey">Enter your email address to register to our newsletter subscription
                    delivered on a regular basis!</p>
            </div>

            <div class="col">

                <div class="input-group mb-3">
                    <button class="btn btn-primary input-group-text">Confirm identity</button>
                    <div class="form-floating">
                        <input type="email" class="form-control" id="SubscribeNewsletter"
                            placeholder="Enter your email">
                        <label for="SubscribeNewsletter">Enter your email</label>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.c-green {
    color: #20AD96;
}
</style>