<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="conatiner py-3">

        <div class="row row-cols-2 align-items-center">

            <div class="col">

                <h3>Subscribe Newsletters</h3>
                <p>Enter your email address to register to our newsletter subscription
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

<style lang="scss" scoped></style>