<template>
  <header>
    <nav class="navbar navbar-expand-lg navbar-light bg-light p-3">
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
              <!-- Dropdown per "Home" con tre colonne -->
              <template v-if="item.name === 'Home'">
                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" aria-expanded="false">
                  {{ item.name }}
                </a>
                <ul class="dropdown-menu p-3 d-flex justify-content-between" style="width: 900px;">
                  <!-- Prima colonna di voci di menu -->
                  <div class="col-4">
                    <li v-for="(subItem, subIndex) in item.submenu.slice(0, 6)" :key="subIndex">
                      <a class="dropdown-item" :href="subItem.link">{{ subItem.name }}</a>
                    </li>
                  </div>

                  <!-- Seconda colonna di voci di menu -->
                  <div class="col-4">
                    <li v-for="(subItem, subIndex) in item.submenu.slice(6, 12)" :key="subIndex">
                      <a class="dropdown-item" :href="subItem.link">{{ subItem.name }}</a>
                    </li>
                  </div>

                  <!-- Terza colonna con immagine -->
                  <div class="col-4 d-flex align-items-center justify-content-center">
                    <img src="../assets/images/homepages-mega-menu-image-alt.jpg" alt="Dropdown Image"
                      class="img-fluid">
                  </div>
                </ul>
              </template>

              <!-- Dropdown normale per gli altri elementi -->
              <template v-else-if="item.submenu">
                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" aria-expanded="false">
                  {{ item.name }}
                </a>
                <ul class="dropdown-menu">
                  <li v-for="(subItem, subIndex) in item.submenu" :key="subIndex">
                    <a class="dropdown-item" :href="subItem.link">{{ subItem.name }}</a>
                  </li>
                </ul>
              </template>

              <!-- Regular link -->
              <template v-else>
                <a class="nav-link" :href="item.link">
                  <i :class="item.icon"></i> {{ item.name }}
                </a>
              </template>
            </li>

            <!-- Search bar -->
            <div class="input-group">
              <input class="form-control" type="search" placeholder="Search..." aria-label="Search">
              <button class="btn btn-outline-success" type="submit">
                <i class="fa-solid fa-magnifying-glass"></i>
              </button>
            </div>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>


<script>
export default {
  name: 'PageHeader',
  data() {
    return {
      menuItems: [
        {
          name: 'Home',
          submenu: [
            { name: 'MaxCoach Education', link: '#' },
            { name: 'Course Portal', link: '#' },
            { name: 'Distant Learning', link: '#' },
            { name: 'Multimedia Pedagogy', link: '#' },
            { name: 'Modern Schooling', link: '#' },
            { name: 'Remote training', link: '#' },
            { name: 'Health Coaching', link: '#' },
            { name: 'Gym Coaching', link: '#' },
            { name: 'Business', link: '#' },
            { name: 'Artist', link: '#' },

            { name: 'Kitchen Coach', link: '#' },
            { name: 'Motivation', link: '#' },
            { name: 'Dancing', link: '#' },
            { name: 'Guitar', link: '#' },
            { name: 'Yoga', link: '#' },
            { name: 'Photography', link: '#' },
            { name: 'Personal Finance', link: '#' },
            { name: 'Sales Coaching', link: '#' },
            { name: 'Mental Therapy', link: '#' },

          ]
        },
        {
          name: 'Pages',
          submenu: [
            { name: 'Start Here', link: '#' },
            { name: 'Success story', link: '#' },
            { name: 'About me', link: '#' },
            { name: 'About us 01', link: '#' },
            { name: 'About us 02', link: '#' },
            { name: 'About us 03', link: '#' },
            { name: 'Contact me', link: '#' },
            { name: 'Contact us', link: '#' },
            { name: 'Purchase Guide', link: '#' },
            { name: 'Privacy Policy', link: '#' },
            { name: 'Terms of Service', link: '#' },
          ]
        },
        {
          name: 'Courses',
          submenu: [
            { name: 'Courses Grid 01', link: '#' },
            { name: 'Courses Grid 02', link: '#' },
            { name: 'Courses Grid 03', link: '#' },
            { name: 'Membership Levels', link: '#' },
            { name: 'Become a Teacher', link: '#' },
            { name: 'Profile', link: '#' },
            { name: 'Checkout', link: '#' },
            { name: 'Single Layout', link: '#' },
          ],
        },
        {
          name: 'Features',
          submenu: [
            { name: 'Events', link: '#' },
            { name: 'Zoom Meetings', link: '#' },
          ]
        },
        {
          name: 'Blog',
          submenu: [
            { name: 'Blog Grid', link: '#' },
            { name: 'Blog Masonry', link: '#' },
            { name: 'Blog Classic', link: '#' },
            { name: 'Blog List', link: '#' },
          ]
        },
        {
          name: 'Shop',
          submenu: [
            { name: 'Shop Left Sidebar', link: '#' },
            { name: 'Shop Right Sidebar', link: '#' },
            { name: 'Cart', link: '#' },
            { name: 'Wishlist', link: '#' },
            { name: 'Single Product', link: '#' },
          ]
        },
        {
          name: '', link: '#', icon: 'fa-regular fa-circle-user'
        }

      ],
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
  opacity: 0;
  transform: translateY(-10px);
  transition: all 0.3s ease;
  border-bottom: 4px solid green;
}

.dropdown-menu.show {
  opacity: 1;
  transform: translateY(0);
}


.dropdown:hover .dropdown-menu {
  visibility: visible;
  opacity: 1;
}

.dropdown {
  padding: 0 15px;
}
</style>
