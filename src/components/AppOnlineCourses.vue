<script>
import OnlineCoursesCard from './OnlineCoursesCard.vue';
    export default {
        data() {
            return {
                featuredOnlineCourses: [
                    {
                        name: 'Personal Finance: Finalcial Security Thinking & Principles',
                        lesson: 2,
                        students: 326,
                        price: 'Free',
                        picPath: '#'
                    },
                    {
                        name: 'Personal Finance: Finalcial Security Thinking & Principles',
                        lesson: 2,
                        students: 326,
                        price: 'Free',
                        picPath: '#'
                    },
                    {
                        name: 'Personal Finance: Finalcial Security Thinking & Principles',
                        lesson: 2,
                        students: 326,
                        price: 'Free',
                        picPath: '#'
                    },
                    {
                        name: 'Personal Finance: Finalcial Security Thinking & Principles',
                        lesson: 2,
                        students: 326,
                        price: 'Free',
                        picPath: '#'
                    },
                    {
                        name: 'Personal Finance: Finalcial Security Thinking & Principles',
                        lesson: 2,
                        students: 326,
                        price: 'Free',
                        picPath: '#'
                    },
                    {
                        name: 'Personal Finance: Finalcial Security Thinking & Principles',
                        lesson: 2,
                        students: 326,
                        price: 'Free',
                        picPath: '#'
                    }
                ]
            }
        },
        components: {
            OnlineCoursesCard
        }
    }
</script>

<template>
    
    <OnlineCoursesCard v-for="((course, index) in featuredOnlineCourses)" :key="index"
    :picPath="course.picPath"
    :price="course.price"
    :students="course.students"
    
    />
    <ComicsCard v-for="(comic, index) in comicsBooks" :key="index"
                :picUrl="comic.thumb"
                :price="comic.price"
                :title="comic.series"
                :bookType="comic.type" />

    <h1 class="text-danger"> ciao</h1>


</template>

<style scoped lang="scss">
 @use '../style/general.scss' as *;
</style>