<script>
import OnlineCourses from './components/AppOnlineCourses.vue';
import Jumbotron from './components/Jumbotron.vue';
import PageHeader from './components/PageHeader.vue';
import EnjoyableSection from './components/AppEnjoyableSection.vue';
import SmartTutoringProgram from './components/SmartTutoringProgram.vue';
import IframeVideos from './components/IframeVideos.vue';
import MainNavBar from './components/MainNavBar.vue';

export default {
  components: {
    OnlineCourses,
    PageHeader,
    EnjoyableSection,
    Jumbotron,
    SmartTutoringProgram,
    IframeVideos,
    MainNavBar
  }
}

</script>

<template>
<<<<<<< HEAD
  <PageHeader :menuItems="menuItems" />
  <Jumbotron />
=======

  <MainNavBar />
  <div>
    <PageHeader :menuItems="menuItems" />
    <Jumbotron title="Distant learning for further expansion"
      subtitle="Learning is a life-long journey that in fact we never find the terminate stop. Stop searching, enjoy the process."
      buttonText="Download free guide" />

  </div>
>>>>>>> origin/OnlineCourses-+-SmartTutoringProgram
  <OnlineCourses />
  <SmartTutoringProgram />
  <IframeVideos />
  <EnjoyableSection />



</template>


<style lang="scss">
@use './style/general.scss' as *;
</style>
