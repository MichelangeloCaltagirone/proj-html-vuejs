<script>
export default {
    data() {
        return {
            OurResults:
                [

                    {
                        name: 'Successfully trained',
                        num: 1790,
                        cose: 'Enrolled Learners'
                    },
                    {
                        name: 'Proudly Received',
                        num: 19,
                        cose: 'Countrywide Awards'
                    },
                    {
                        name: 'Firmly Established',
                        num: 24,
                        cose: 'local branches'
                    },
                    {
                        name: 'Getting Featured on',
                        num: 1090,
                        cose: 'Blog Posts'
                    },
                ]

        }
    }
}
</script>

<template>
    <div class="row row-cols-4">

        <div class="col" v-for="result in OurResults">
            <h3>{{ result.name }}</h3>
            <span>{{ result.num }}</span>
            <span>{{ result.cose }}</span>
        </div>
    </div>
</template>

<style lang="scss" scoped></style>