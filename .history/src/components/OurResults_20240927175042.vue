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
                ],
        }
    }
}
</script>

<template>
    <section class="p-5">


        <div class="container-fluid">
            <div class="row row-cols-sm row-cols-md-5 row-cols-xl-4">

                <div class="col" v-for="result in OurResults">
                    <div class="wrapper">
                        <h2>{{ result.name }}</h2>
                        <span class="numb display-1">{{ result.num }}</span>
                        <span class="cose fs-5">{{ result.cose }}</span>
                    </div>

                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.row {
    height: 40vh;

    .col {
        display: flex;
        align-items: center;
        justify-content: center;

        .wrapper {
            display: flex;
            width: calc(90% /2 + 1.6rem);
            flex-direction: column;
            align-items: center;

            h2 {
                font-weight: 600;
                word-wrap: normal;

                text-align: center;
                color: #3F3A64;
            }

            .numb {
                font-weight: 800;
                color: #20AD96;
            }

            .cose {
                font-weight: 700;
                text-wrap: nowrap;
                letter-spacing: 2px;
                color: #8C89A2;
            }
        }
    }

}
</style>