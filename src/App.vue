<script>
import OnlineCourses from './components/AppOnlineCourses.vue';
import Jumbotron from './components/Jumbotron.vue';
import PageHeader from './components/PageHeader.vue';
import EnjoyableSection from './components/AppEnjoyableSection.vue';
import SmartTutoringProgram from './components/SmartTutoringProgram.vue';
import IframeVideos from './components/IframeVideos.vue';
import MainNavBar from './components/MainNavBar.vue';
import SubscribeNewsletter from './components/subscribeNewsletterSection.vue';

export default {
  components: {
    OnlineCourses,
    PageHeader,
    EnjoyableSection,
    Jumbotron,
    SmartTutoringProgram,
    IframeVideos,
    MainNavBar,
    SubscribeNewsletter
  }
}

</script>

<template>
  <MainNavBar />
  <div>
    <PageHeader :menuItems="menuItems" />
    <Jumbotron />
  </div>
  <OnlineCourses />
  <SmartTutoringProgram />
  <IframeVideos />
  <EnjoyableSection />
  <SubscribeNewsletter />


</template>


<style lang="scss">
@use './style/general.scss' as *;
</style>
