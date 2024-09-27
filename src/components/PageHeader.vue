<template>
  <header>
    <MainNavBar />
    <nav class="navbar navbar-expand-lg navbar-light p fixed-top bg-light">
      <div class="container">
        <!-- Logo -->
        <a class="navbar-brand" href="#">
          <img src="../assets/images/dark-logo.png" alt="MaxCoach Logo" />
        </a>

        <!-- Button toggle for mobile view -->
        <button class="navbar-toggler" type="button" @click="toggleSidebar" aria-controls="sidebar"
          aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>

        <!-- Navbar links for larger screens-->
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
                    <li v-for="(subItem, subIndex) in item.submenu.slice(0, 10)" :key="subIndex">
                      <a class="dropdown-item" :href="subItem.link">{{ subItem.name }}
                        <span v-if="subItem.label" class="badge"
                          :class="{ 'bg-danger': subItem.label === 'Hot', 'bg-success': subItem.label === 'New' }">
                          {{ subItem.label }}
                        </span>
                      </a>
                    </li>
                  </div>

                  <!-- Seconda colonna di voci di menu -->
                  <div class="col-4">
                    <li v-for="(subItem, subIndex) in item.submenu.slice(10, 19)" :key="subIndex">
                      <a class="dropdown-item" :href="subItem.link">{{ subItem.name }}
                        <span v-if="subItem.label" class="badge"
                          :class="{ 'bg-danger': subItem.label === 'Hot', 'bg-success': subItem.label === 'New' }">
                          {{ subItem.label }}
                        </span>
                      </a>
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
                    <a class="dropdown-item" :href="subItem.link">{{ subItem.name }}
                      <!-- Mostra l'etichetta se esiste -->
                      <span v-if="subItem.label" class="badge"
                        :class="{ 'bg-danger': subItem.label === 'HOT', 'bg-success': subItem.label === 'NEW' }">
                        {{ subItem.label }}
                      </span>
                    </a>
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

    <!-- Sidebar component -->
    <Sidebar :isVisible="isSidebarVisible" @close-sidebar="toggleSidebar" :menuItems="menuItems" />

    <!-- aggiunta jumbotron -->
    <Jumbotron />
  </header>
</template>


<script>
// Importa il componente Jumbotron e SideBar
import Jumbotron from './Jumbotron.vue';
import Sidebar from './SideBar.vue';
import MainNavBar from './MainNavBar.vue';

export default {
  name: 'PageHeader',
  components: {
    Jumbotron, // Registrazione del componente Jumbotron
    Sidebar, // Registrazione del componente SideBar
    MainNavBar // Registrazione del componente MainNavBar
  },
  data() {
    return {
      isSidebarVisible: false,
      menuItems: [
        {
          name: 'Home',
          submenu: [
            { name: 'MaxCoach Education', link: '#', label: 'Hot' },
            { name: 'Course Portal', link: '#' },
            { name: 'Distant Learning', link: '#', label: 'Hot' },
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
            { name: 'Sales Coaching', link: '#', label: 'New' },
            { name: 'Mental Therapy', link: '#', label: 'New' },

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
  },
  methods: {
    toggleSidebar() {
      this.isSidebarVisible = !this.isSidebarVisible;
    },
  },
  // mounted() {
  //   console.log(this.menuItems)
  // }
};
</script>

<style scoped>
.navbar-nav .nav-link {
  color: #000;
  position: relative;
  transition: color 0.5s ease;
}

.navbar-nav .nav-link:hover {
  color: #28a745;
}

/* Linea verde sotto al link, che si riempie gradualmente */
.navbar-nav .nav-link::before {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 1px;
  background-color: #28a745;
  transition: width 0.5s ease;
}

/* La linea si riempie quando si fa hover */
.navbar-nav .nav-link:hover::before {
  width: 100%;
}


/* Dropdown menu inizialmente nascosto */
.dropdown-menu {
  opacity: 0;
  visibility: hidden;
  transition: all 0.5s ease;
  border-bottom: 4px solid green;
  /* transform: translateY(20); */
}

/* Mostra il dropdown quando la linea è completamente riempita */
.navbar-nav .nav-link:hover::before {
  width: 100%;
}


.dropdown-menu:hover .dropdown {
  opacity: 1;
  visibility: visible;
}

.navbar-brand img {
  width: 160px;
}

.navbar .dropdown:hover .dropdown-menu {
  display: block;
  margin-top: 0;
}


.dropdown:hover .dropdown-menu {
  visibility: visible;
  opacity: 1;
}

.dropdown {
  padding: 0 15px;
}

header {
  background-color: #fff;
}

.badge {
  margin-left: 5px;
  color: white;
}

/* Specifiche per i badge Hot e New */
.bg-danger {
  background-color: red !important;
}

.bg-success {
  background-color: green !important;
}
</style>
