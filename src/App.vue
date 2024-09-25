<script>
import OnlineCourses from './components/AppOnlineCourses.vue';
import PageHeader from './components/PageHeader.vue';
export default {
  data() {
    return {

    }
  },
  components: {
    OnlineCourses,
    PageHeader
  }
}

</script>

<template>

  <OnlineCourses />

</template>

<style lang="scss">
@use './style/general.scss' as *;
</style>
