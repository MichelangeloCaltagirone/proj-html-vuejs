<template>
  <header>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="container">
        <!-- Logo -->
        <a class="navbar-brand" href="#">
          <img src="../assets/images/dark-logo.png" alt="MaxCoach Logo" />
        </a>

        <!-- Button toggle for mobile view -->
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>

        <!-- Navbar links -->
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li v-for="(item, index) in menuItems" :key="index" class="nav-item">
              <a class="nav-link" :href="item.link">{{ item.name }}</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'PageHeader',
  props: {
    menuItems: {
      type: Array,
      required: true
    }
  }
};
</script>

<style scoped>
.navbar-brand img {
  width: 120px;
}
</style>
