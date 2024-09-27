<script>
import OnlineCoursesCard from './OnlineCoursesCard.vue';
    export default {
        data() {
            return {
                featuredOnlineCourses: [
                    {
                        name: 'Personal Finance: Finalcial Security Thinking & Principles',
                        lessons: 2,
                        students: 326,
                        price: 'Free',
                        picPath: 'course-featured-image-01-480x298.jpg'
                    },
                    {
                        name: 'Learning to Write as a Professional Author',
                        lessons: 20,
                        students: 81,
                        price: 'Free',
                        picPath: 'course-02-480x298.jpg'
                    },
                    {
                        name: 'Costumer-centric Info-Tech Strategies',
                        lessons: 24,
                        students: 972,
                        price: 'Free',
                        picPath: 'stock-full-hd-03-480x298.jpg'
                    },
                    {
                        name: 'Open Programming Courses for Everyone: Phython',
                        lessons: 17,
                        students: 66,
                        price: '$19.00',
                        picPath: 'stock-full-hd-04-480x298.jpg'
                    },
                    {
                        name: 'Accademic Listening and Note-taking',
                        lessons: 14,
                        students: 73,
                        price: 'Free',
                        picPath: 'stock-full-hd-05-480x298.jpg'
                    },
                    {
                        name: 'Master JQuery in a Short Period of Time',
                        lessons: 6,
                        students: 51,
                        price: '$39.00',
                        picPath: 'stock-full-hd-06-480x298.jpg'
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

            <h5 class="text-center">STIMULATED TO LEARN?</h5>
            <h1 class="text-center mb-5">Featured Online Courses</h1>
            
        <div class="courseList d-flex flex-wrap row-cols-1 row-cols-lg-2">
            <OnlineCoursesCard v-for="(course, index) in featuredOnlineCourses" :key="index"
            :picPath="course.picPath"
            :price="course.price"
            :students="course.students"
            :lessons="course.lessons"
            :name="course.name" />
        </div>
        
        <div class="d-flex justify-content-center my-4">
            <button type="button" class="btn btn-large mx-auto">View all courses<i class="fa-solid fa-arrow-right-long"></i></button>
        </div>
    </div>

   </div>
   
   
   
</template>

<style scoped lang="scss">
.bg-color {
    background-color: #F5F7FA;
}
.btn {  
        padding: 15px 45px;
        background-color: #20AD96;
        color: white;
        font-size: 12px;
        font-weight: bold;
}
h5 {
    color: #8C89A2;
}

</style>