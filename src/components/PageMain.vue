<script>
import OnlineCourses from './AppOnlineCourses.vue';
import EnjoyableSection from './AppEnjoyableSection.vue';
import SmartTutoringProgram from './SmartTutoringProgram.vue';
import IframeVideos from './IframeVideos.vue';
import SubscribeNewsletter from './subscribeNewsletterSection.vue';
import OurResults from './OurResults.vue';
import DynamicSliderVue from './DynamicSlider.vue';

    export default {
        data() {
            return {

            }
        },
        components: {
            OnlineCourses,
            EnjoyableSection,
            SmartTutoringProgram,
            IframeVideos,
            DynamicSliderVue,
            SubscribeNewsletter,
            OurResults            
        }
    }

</script>

<template>

    <OnlineCourses />
    <SmartTutoringProgram />
    <IframeVideos />
    <DynamicSliderVue/>
    <OurResults />
    <EnjoyableSection />
    <SubscribeNewsletter />


</template>

<style scoped>
</style>