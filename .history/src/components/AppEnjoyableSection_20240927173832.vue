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

        <div class="container py-5">

            <div class="row row-cols-3 gx-5">

                <div class="col-md-2 col-xl-3">
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

                <div class="blog col-md-5 col-xl-" v-for="(blog, index) in Blogs" :key="index">
                    <div class="card">
                        <div class="img-wrapper"></div>
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

                    .fa-arrow-right {
                        animation: slide-in-left 0.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;

                        .fa-arrow-right {
                            animation: slide-in-right 0.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
                        }
                    }
                }

            }
        }


        @keyframes slide-in-left {
            0% {
                transform: translateX(-1000px);
                opacity: 0;
            }

            100% {
                transform: translateX(0);
                opacity: 1;
            }
        }



        @keyframes slide-in-right {
            0% {
                transform: translateX(1000px);
                opacity: 0;
            }

            100% {
                transform: translateX(0);
                opacity: 1;
            }
        }





    }

}




.col {

    .card {
        max-width: 300px;
        max-height: 450px;

        &:hover {
            .img-wrapper {
                width: 100%;
                overflow: hidden;
                display: inline-block;
                box-sizing: border-box;
                border: 1px solid #000;


                img {
                    animation: scale-up-center 3s linear both {}

                }
            }



            @keyframes scale-up-center {
                0% {
                    -webkit-transform: scale(1);
                    transform: scale(1)
                }

                100% {
                    -webkit-transform: scale(1.5);
                    transform: scale(1.5)
                }
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
</style>