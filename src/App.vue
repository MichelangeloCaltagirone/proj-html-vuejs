<script>
import OnlineCourses from './components/AppOnlineCourses.vue';
import EnjoyableSection from './components/AppEnjoyableSection.vue';
export default {
  data() {
    return {

    }
  },
  components: {
    OnlineCourses,
    EnjoyableSection
  }
}

</script>

<template>

  <OnlineCourses />
  <EnjoyableSection />
</template>

<style lang="scss">
@use './style/general.scss' as *;
</style>
