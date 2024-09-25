<script>
import OnlineCourses from './components/AppOnlineCourses.vue';
import Jumbotron from './components/Jumbotron.vue';
import PageHeader from './components/PageHeader.vue';
import SmartTutoringProgram from './components/SmartTutoringProgram.vue';

export default {
  data() {
    return {

    }
  },
  components: {
    OnlineCourses,
    PageHeader,
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
  <SmartTutoringProgram />

</template>

<style lang="scss">
@use './style/general.scss' as *;
</style>
