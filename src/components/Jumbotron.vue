<template>
  <div class="jumbotron text-dark p-5 mt-5">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-md-6 order-2 order-md-1">
          <h1 class="display-4">{{ title }}</h1>
          <p class="lead">{{ subtitle }}</p>
          <a href="#" class="btn btn-success">
            <i class="fa-solid fa-download"></i>
            {{ buttonText }}
          </a>


          <p class="d-flex align-items-center mb-0 mt-3">
            <span class="me-2">Have question?</span>
            <a href="#" class="btn question-link">Get Free Sample
              <i class="ms-2 fa-solid fa-arrow-right-long"></i>
            </a>
          </p>

        </div>

        <div class="col-md-6 order-1 order-md-2">
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
h1 {
  font-weight: bold;
  color: #3F3A64;
}

.lead {
  font-weight: 400;
  color: #696969;
}

.image-wrapper {
  padding: 10px;
  display: inline-block;
  text-align: center;
}

.jumbotron {
  background-color: #f5f7fA;
}

/* Stile per il link */
.question-link {
  color: #28a745;
  position: relative;
  display: inline-block;
  text-decoration: none;
  transition: color 0.5s ease;
}

.question-link:before {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 1px;
  background-color: grey;
  transform: scaleX(1);
  transform-origin: bottom left;
  transition: transform 0.5s ease, background-color 0.5s ease;
}

.question-link::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 2px;
  background-color: #28a745;
  transform: scaleX(0);
  transform-origin: bottom left;
  transition: transform 0.5s ease, background-color 0.5s ease;
}

.question-link:hover::after {
  transform: scaleX(1);
  background-color: #28a745;
}
</style>
