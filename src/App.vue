<script>
import OnlineCourses from './components/AppOnlineCourses.vue';
import Jumbotron from './components/Jumbotron.vue';
import PageHeader from './components/PageHeader.vue';
import EnjoyableSection from './components/AppEnjoyableSection.vue';
import SmartTutoringProgram from './components/SmartTutoringProgram.vue';
import IframeVideos from './components/IframeVideos.vue';

export default {
  components: {
    OnlineCourses,
    PageHeader,
    EnjoyableSection,
    Jumbotron,
    SmartTutoringProgram,
    IframeVideos
  }
}

</script>

<template>
  <PageHeader :menuItems="menuItems" />
  <Jumbotron />
  <OnlineCourses />
  <SmartTutoringProgram />
  <IframeVideos />
  <EnjoyableSection />



</template>


<style lang="scss">
@use './style/general.scss' as *;
</style>
