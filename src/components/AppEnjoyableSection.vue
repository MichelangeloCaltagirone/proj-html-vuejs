<script>
export default {
    data() {
        return {

            insinghts: [
                {
                    link: " Become a Better Blogger: Content Planning",

                },

                {
                    link: "Promoting Your Online Business on Pinterest",

                },

                {
                    link: "Gamification and Game- Based Learning",

                },

                {
                    link: "Designing an Online Course from Experts Perspective",

                },

                {
                    link: "Why Online Courses Are the Future of Education",

                },


            ],
        }
    }, methods: {
        getImgUrl(index) {
            return new URL(`../assets/img/img${index}.jpg`, import.meta.url).href
        },
    }
}
</script>

<template>
    <section>

        <div class="container py-4">

            <div class="row row-cols-3 gx-5">

                <div class="col">
                    <span class="text-secondary fs-5">Enjoyable <span class="text-bg-success">insights</span></span>

                    <div class="fw-bold fs-3">Most Viewed <span class="text-success">Best Blogs</span></div>
                    <ul class="">
                        <li v-for="item in insinghts">
                            <a class="fs-5 fw-bold" href="#">{{ item.icon }}
                                <span>{{ item.link }}</span>
                            </a>
                        </li>
                    </ul>
                </div>

                <div class="col" v-for="(x, index) in 2">
                    <div class="card" style="width: 18rem;">
                        <img :src="getImgUrl(index)" class="card-img-top" alt="team-6 classe-131">
                        <div class="card-body">

                            <p class="card-text" v-if="index == 0">"Determinazione, Unità, Eccellenza. Team 6 Classe 131
                                apre la strada, inarrestabile!"</p>
                            <p v-else>
                                "Forza nel codice, guidati dalla passione. Non siamo solo bravi, siamo i migliori!"</p>
                        </div>
                    </div>

                </div>

            </div>
        </div>


    </section>
</template>

<style lang="scss" scoped>
section {
    background-color: #F5F1ED;

    ul {
        list-style: none;
        padding: 0%;



        li {
            margin: 15px 0;

            a {
                text-decoration: none;
                color: inherit;

                &:hover,
                >*:hover {
                    color: #198754;

                }


                &::before {
                    content: '\2190';
                }
            }
        }
    }


}
</style>