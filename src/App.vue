<script>
import OnlineCourses from './components/AppOnlineCourses.vue';
import Jumbotron from './components/Jumbotron.vue';
import PageHeader from './components/PageHeader.vue';
import EnjoyableSection from './components/AppEnjoyableSection.vue';
import SmartTutoringProgram from './components/SmartTutoringProgram.vue';

export default {
  data() {
    return {
      menuItems: [
        {
          name: 'Home',
          submenu: [
            { name: 'MaxCoach Education', link: '#' },
            { name: 'Course Portal', link: '#' },
            { name: 'Distant Learning', link: '#' },
            { name: 'Multimedia Pedagogy', link: '#' },
            { name: 'Modern Schooling', link: '#' },
            { name: 'Remote training', link: '#' },
            { name: 'Health Coaching', link: '#' },
            { name: 'Gym Coaching', link: '#' },
            { name: 'Business', link: '#' },
            { name: 'Artist', link: '#' },

            { name: 'Kitchen Coach', link: '#' },
            { name: 'Motivation', link: '#' },
            { name: 'Dancing', link: '#' },
            { name: 'Guitar', link: '#' },
            { name: 'Yoga', link: '#' },
            { name: 'Photography', link: '#' },
            { name: 'Personal Finance', link: '#' },
            { name: 'Sales Coaching', link: '#' },
            { name: 'Mental Therapy', link: '#' },

          ]
        },
        {
          name: 'Pages',
          submenu: [
            { name: 'Start Here', link: '#' },
            { name: 'Success story', link: '#' },
            { name: 'About me', link: '#' },
            { name: 'About us 01', link: '#' },
            { name: 'About us 02', link: '#' },
            { name: 'About us 03', link: '#' },
            { name: 'Contact me', link: '#' },
            { name: 'Contact us', link: '#' },
            { name: 'Purchase Guide', link: '#' },
            { name: 'Privacy Policy', link: '#' },
            { name: 'Terms of Service', link: '#' },
          ]
        },
        {
          name: 'Courses',
          submenu: [
            { name: 'Courses Grid 01', link: '#' },
            { name: 'Courses Grid 02', link: '#' },
            { name: 'Courses Grid 03', link: '#' },
            { name: 'Membership Levels', link: '#' },
            { name: 'Become a Teacher', link: '#' },
            { name: 'Profile', link: '#' },
            { name: 'Checkout', link: '#' },
            { name: 'Single Layout', link: '#' },
          ],
        },
        {
          name: 'Features',
          submenu: [
            { name: 'Events', link: '#' },
            { name: 'Zoom Meetings', link: '#' },
          ]
        },
        {
          name: 'Blog',
          submenu: [
            { name: 'Blog Grid', link: '#' },
            { name: 'Blog Masonry', link: '#' },
            { name: 'Blog Classic', link: '#' },
            { name: 'Blog List', link: '#' },
          ]
        },
        {
          name: 'Shop',
          submenu: [
            { name: 'Shop Left Sidebar', link: '#' },
            { name: 'Shop Right Sidebar', link: '#' },
            { name: 'Cart', link: '#' },
            { name: 'Wishlist', link: '#' },
            { name: 'Single Product', link: '#' },
          ]
        }
      ],
    }
  },
  components: {
    OnlineCourses,
    PageHeader,
    EnjoyableSection,
    Jumbotron,
    SmartTutoringProgram
  }
}

</script>

<template>

  <div>
    <PageHeader :menuItems="menuItems" />
    <Jumbotron title="Distant learning for further expansion"
      subtitle="Learning is a life-long journey that in fact we never find the terminate stop. Stop searching, enjoy the process."
      buttonText="Download free guide" />

  </div>
  <OnlineCourses />
  <EnjoyableSection />
  <SmartTutoringProgram />

</template>


<style lang="scss">
@use './style/general.scss' as *;
</style>
