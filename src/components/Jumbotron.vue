<template>
  <div class="jumbotron bg-light text-dark p-5">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-md-6">
          <h1 class="display-4">{{ title }}</h1>
          <p class="lead">{{ subtitle }}</p>
          <a href="#" class="btn btn-success">{{ buttonText }}</a>
        </div>
        <div class="col-md-6">
          <img src="../assets/images/about-me-profile-ohm4dxoearqbxny7q3bq1pzbdgofdx0tobbeqcvzd0.jpg"
            alt="Jumbotron Image" class="img-fluid rounded-circle">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Jumbotron',
  props: {
    title: {
      type: String,
      required: true
    },
    subtitle: {
      type: String,
      required: true
    },
    buttonText: {
      type: String,
      required: true
    }
  }
};
</script>

<style scoped></style>
