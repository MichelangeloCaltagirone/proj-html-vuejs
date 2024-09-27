<script>
import OnlineCourses from './components/AppOnlineCourses.vue';
import PageHeader from './components/PageHeader.vue';
import EnjoyableSection from './components/AppEnjoyableSection.vue';
import SmartTutoringProgram from './components/SmartTutoringProgram.vue';
import IframeVideos from './components/IframeVideos.vue';

import SubscribeNewsletter from './components/subscribeNewsletterSection.vue';
import OurResults from './components/OurResults.vue';

export default {
  components: {
    OnlineCourses,
    PageHeader,
    EnjoyableSection,
    SmartTutoringProgram,
    IframeVideos,
    SubscribeNewsletter,
    OurResults,
  }
}

</script>

<template>
  <MainNavBar />

  <PageHeader />

  <OnlineCourses />
  <SmartTutoringProgram />
  <IframeVideos />
  <OurResults />
  <EnjoyableSection />
  <SubscribeNewsletter />


</template>


<style lang="scss">
@use './style/general.scss' as *;
</style>
