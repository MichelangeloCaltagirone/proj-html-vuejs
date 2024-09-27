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
                        title: 'ARTIST',
                        image: 'artist-blog-01-480x352.jpg',
                        previewText: 'Brush Strokes Energize Trees in Paintings',
                        link: '#',
                        date: 'May 15, 2020',
                        views: 688,

                    },

                    {
                        title: 'ARTIST',
                        image: 'artist-blog-03-480x352.jpeg',
                        previewText: 'Pocket-Sized Notebooks Hold Miniature Paintings',
                        link: '#',
                        date: 'May 15, 2020',
                        views: 603,

                    },

                ],
        }

    },
    methods: {
        getImgUrl(imagePath) {
            return new URL(`../assets/images/${imagePath}`, import.meta.url).href
        },
    }
}
</script>

<template>
    <section class="p-5">

        <div class="container-fluid py-5">

            <div class="row row-cols-3 gx-5">

                <div class="col">
                    <div class="c-grey fs-4 mb-2">Enjoyable <span class="c-green">insights</span></div>

                    <div class="fw-bold fs-1 text-nowrap mb-5">Most Viewed <span class="c-green fw-medium fs-1">Best
                            Blogs</span></div>
                    <ul>
                        <li v-for="item in bestBlogs">
                            <a class="fw-bold" :href="item.link">
                                <i class="fa-solid fa-arrow-right"></i>
                                <span>{{ item.name }}</span>
                            </a>
                        </li>
                    </ul>
                </div>

                <div class="blog col" v-for="(blog, index) in Blogs" :key="index">
                    <div class="card">
                        <img :src="getImgUrl(blog.image)" class="card-img-top" alt="">
                        <div class="card-body d-flex flex-column">
                            <h3 class="c-grey">{{ blog.title }}</h3>
                            <p>{{ blog.previewText }}</p>
                            <span class="c-grey">
                                <i class="fa-regular fa-calendar"></i>
                                {{ blog.date }}
                            </span>
                            <span class="c-grey">
                                <i class="fa-solid fa-eye"></i>
                                {{ blog.views }}
                            </span>
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
    color: #3F3A64;

    ul {
        list-style: none;
        padding: 0%;



        li {
            margin: 15px 0;

            a {
                text-decoration: none;
                color: inherit;
                font-size: 20px;
                line-height: 3rem;

                &:hover,
                >*:hover {
                    color: #20AD96;

                }

            }

            .col {

                .card {
                    height: 400px;
                    width: 250px;
                }
            }
        }


    }


    .c-grey {
        color: #8C89A2;
    }

    .c-green {
        color: #20AD96;
    }

}
</style>