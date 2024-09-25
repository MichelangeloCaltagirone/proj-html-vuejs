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
                        picPath: './assets/images/course-featured-image-01-480x298.jpg'
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
   <div class="bg-color">
    <div class="container py-5"> 
    <div class="courseList d-flex flex-wrap row-cols-2">
        <OnlineCoursesCard v-for="(course, index) in featuredOnlineCourses" :key="index"
        :picPath="course.picPath"
        :price="course.price"
        :students="course.students"
        :lessons="course.lessons"
        :name="course.name" />
    </div>
    </div>

   </div> 
   
</template>

<style scoped lang="scss">
.bg-color {
    background-color: red
}
</style>