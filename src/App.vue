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
        { name: 'Home', link: '#' },
        { name: 'Pages', link: '#' },
        { name: 'Courses', link: '#' },
        { name: 'Features', link: '#' },
        { name: 'Blog', link: '#' },
        { name: 'Shop', link: '#' },
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
