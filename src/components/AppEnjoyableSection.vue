<script>
export default {
    data() {
        return {

            insinghts: [
                {
                    link: " Become a Better Blogger: Content Planning",
                    icon: "2190",
                },

                {
                    link: "Promoting Your Online Business on Pinterest",
                    icon: "2190",
                },

                {
                    link: "Gamification and Game- Based Learning",
                    icon: "2190",
                },

                {
                    link: "Designing an Online Course from Experts Perspective",
                    icon: "2190",
                },

                {
                    link: "Why Online Courses Are the Future of Education",
                    icon: "2190",
                },


            ],
        }
    },

}
</script>

<template>
    <section>

        <div class="conatiner">


            <div class="row">

                <div class="col">
                    <span>Enjoyable insights</span>

                    <h3>Most Viewed Best Blogs</h3>
                    <ul>
                        <li v-for="item in insinghts">{{ item.link }}</li>
                    </ul>
                </div>
                <div class="col center card">

                    <div class="card">
                        <div class="fakeImg"></div>
                        <div class="card-text"></div>
                    </div>

                </div>
            </div>
            <div class="col right">
                <div class="card">
                    <div class="fakeImg"></div>
                    <div class="card-text"></div>
                </div>

            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
section {
    background-color: #F5F1ED;

    .container {
        max-width: 1200px;
        margin: 0 auto;

        .row {
            display: flex;
            flex-direction: row;


            .col {
                flex-basis: calc(100% / 3);

                ul {
                    list-style-type: none;
                }
            }

            .card {
                height: 250px;
                width: 200;

            }

        }
    }
}
</style>