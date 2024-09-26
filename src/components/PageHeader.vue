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
            <li v-for="(item, index) in menuItems" :key="index" class="nav-item dropdown"
              :class="{ 'dropdown': item.submenu }">
              <!-- Dropdown link -->
              <template v-if="item.submenu">
                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" aria-expanded="false">
                  {{ item.name }}
                </a>
                <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                  <li v-for="(subItem, subIndex) in item.submenu" :key="subIndex">
                    <a class="dropdown-item" :href="subItem.link">{{ subItem.name }}</a>
                  </li>
                  <li v-if="item.image">
                    <img :src="item.image" alt="Dropdown Image" class="dropdown-item img-fluid"
                      style="max-width: 100px;">
                  </li>
                </ul>
              </template>

              <!-- Regular link -->
              <template v-else>
                <a class="nav-link" :href="item.link">{{ item.name }}</a>
              </template>
            </li>

            <!-- Search bar -->
            <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
            <button class="btn btn-outline-success" type="submit">Search</button>
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

.navbar .dropdown:hover .dropdown-menu {
  display: block;
  margin-top: 0;
}

.dropdown-menu {
  transition: opacity 0.3s ease;
  opacity: 0;
  visibility: hidden;
}

.dropdown:hover .dropdown-menu {
  visibility: visible;
  opacity: 1;
}
</style>
