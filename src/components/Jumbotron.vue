<template>
  <div class="jumbotron bg-light text-dark p-5">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-md-6">
          <h1 class="display-4">{{ title }}</h1>
          <p class="lead">{{ subtitle }}</p>
          <a href="#" class="btn btn-success">
            <i class="fa-solid fa-download"></i>
            {{ buttonText }}</a>
        </div>
        <div class="col-md-6">
          <img src="../assets/images/about-me-profile-ohm4dxoearqbxny7q3bq1pzbdgofdx0tobbeqcvzd0.jpg"
            alt="Jumbotron Image" class="img-fluid rounded-circle">
        </div>
      </div>
      <!-- Immagini in fila -->
      <div class="container mt-5">
        <div class="row text-center d-flex justify-content-between">
          <div class="col-md-2" v-for="n in 6" :key="n">
            <img :src="`src/assets/images/client-logo-0${n}.png`" class="img-fluid" alt="Image">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Jumbotron',
  data() {
    return {
      title: 'Distant learning for further expansion',
      subtitle: 'Learning is a life-long journey that in fact we never find the terminate stop. Stop searching, enjoy the process.',
      buttonText: 'Download free guide',
    };
  }
};
</script>

<style scoped>
.image-wrapper {
  padding: 10px;
  display: inline-block;
  text-align: center;
}
</style>
