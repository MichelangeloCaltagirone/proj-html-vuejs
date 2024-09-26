<script>
export default {
    data() {
        return {

            bestBlogs: [
                {
                    name: " Become a Better Blogger: Content Planning",
                    link: '#',

                },

                {
                    name: "Promoting Your Online Business on Pinterest",
                    link: '#',

                },

                {
                    name: "Gamification and Game- Based Learning",
                    link: '#',

                },

                {
                    name: "Designing an Online Course from Experts Perspective",
                    link: '#',

                },

                {
                    name: "Why Online Courses Are the Future of Education",
                    link: '#',

                },

            ],

            Blogs:
                [

                    {
                        title: 'BUSSINES',
                        previewText: 'Ten Benefits Of Rentals That May Change Your Perspective',
                        link: '#',
                        date: 'Dec 28, 2020',
                        views: '3,459',

                    },
                    {
                        title: 'BUSSINES',
                        previewText: '10 Things Successful Mompreneurs Do Different',
                        link: '#',
                        date: 'Dec 28, 2020',
                        views: '3,024',

                    },

                ],
        }

    },
    methods: {
        getImgUrl(index) {
            return new URL(`../assets/InsectionSectionImages/home-personal-finance-blog-${index}.jpg`, import.meta.url).href
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
                        <li v-for="item in bestBlogs">
                            <a class="fs-5 fw-bold" :href="item.link">{{ item.icon }}
                                <span>{{ item.name }}</span>
                            </a>
                        </li>
                    </ul>
                </div>

                <div class="blog col" v-for="(blog, index) in Blogs" :key="index">
                    <div class="card" style="width: 18rem;">
                        <img :src="getImgUrl(index)" class="card-img-top" alt="">
                        <div class="card-body d-flex flex-column">
                            <h3>{{ blog.title }}</h3>
                            <p>{{ blog.previewText }}</p>
                            <span>{{ blog.date }}</span>
                            <span>{{ blog.views }} views</span>
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