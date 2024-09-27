<template>
  <div class="sidebar" v-if="isVisible">
    <!-- Header della Sidebar -->
    <div class="sidebar-header">
      <img src="../assets/images/dark-logo.png" alt="Logo" class="logo" />
      <button class="btn-close" @click="toggleSidebar">
        <img src="../assets/images/close.svg" alt="Close" />
      </button>
    </div>

    <!-- Navbar -->
    <ul class="navbar-nav">
      <li v-for="(item, index) in menuItems" :key="index" class="nav-item" :class="{ 'is-open': item.isOpen }">
        <!-- Navigazione principale -->
        <div class="nav-link" @click="toggleDropdown(item)">
          {{ item.name }}
          <span class="dropdown-arrow" v-if="item.submenu">▼</span>
        </div>

        <!-- Dropdown -->
        <ul v-if="item.isOpen" class="dropdown-menu">
          <li v-for="(subItem, subIndex) in item.submenu" :key="subIndex" class="dropdown-item">
            {{ subItem.name }}
            <span v-if="subItem.label" class="badge"
              :class="{ 'bg-danger': subItem.label === 'Hot', 'bg-success': subItem.label === 'New' }">
              {{ subItem.label }}
            </span>
          </li>
        </ul>

        <!-- Linea divisoria tra gli elementi -->
        <hr v-if="index < menuItems.length - 1" />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    isVisible: {
      type: Boolean,
      default: false
    },
    menuItems: {
      type: Array,
      required: true
    }
  },
  methods: {
    toggleSidebar() {
      this.$emit('close-sidebar');
    },
    toggleDropdown(item) {
      // Chiude gli altri dropdown se aperti
      this.menuItems.forEach(i => {
        if (i !== item) i.isOpen = false; // Chiude altri dropdown
      });
      item.isOpen = !item.isOpen; // Apre/chiude il dropdown cliccato
    }
  }
};
</script>


<style scoped>
/* Sidebar */
.sidebar {
  position: fixed;
  top: 0;
  right: 0;
  width: 350px;
  height: 100%;
  background-color: #fff;
  box-shadow: -2px 0 5px rgba(0, 0, 0, 0.1);
  z-index: 1050;
  padding: 20px;
  transition: transform 0.3s ease;
  overflow-y: hidden;
  overflow-x: hidden;
  background-image: url('../assets/images/mobile-bg.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

/* Sovrapposizione viola semitrasparente */
.sidebar:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(78, 72, 110, 0.7);
  /* Sovrapposizione viola */
  z-index: 1;
}

/* Stile per il pulsante di chiusura (X) */
.sidebar .btn-close {
  position: absolute;
  top: 10px;
  right: 10px;
  font-size: 20px;
  border: none;
  background: none;
  z-index: 2;
  cursor: pointer;
  transition: opacity 0.3s ease;
}

/* Logo */
.logo {
  height: 30px;
  z-index: 2;
}

/* Bottone di chiusura (animazione con hover) */
.btn-close img {
  width: 30px;
  transition: transform 0.3s ease, opacity 0.3s ease;
}

.btn-close:hover img {
  transform: rotate(360deg);
  opacity: 0.7;
}

/* Stile per i link della navbar */
.navbar-nav .nav-item .nav-link {
  padding: 10px;
  color: #fff;
  text-decoration: none;
  display: block;
  transition: color 0.3s ease;
  z-index: 2;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

/* Hover sui link della navbar */
.navbar-nav .nav-item .nav-link:hover {
  color: #28a745;
}

/* Dropdown Arrow */
.dropdown-arrow {
  margin-left: 5px;
  transition: transform 0.3s ease;
  cursor: pointer;
}

/* Rotazione freccia quando il dropdown è aperto */
.nav-item.is-open .dropdown-arrow {
  transform: rotate(180deg);
}

/* Dropdown Menu */
.dropdown-menu {
  background-color: rgba(78, 72, 110, 0.7);
  padding: 10px;
  border-radius: 5px;
  margin-top: 5px;
  display: none;
  position: relative;
  z-index: 2;
}

.nav-item.is-open .dropdown-menu {
  display: block;
  z-index: 3;
}

/* Dropdown Items */
.dropdown-item {
  color: #fff;
  padding: 5px 0;
  text-decoration: none;
  z-index: 3;
}

.dropdown-item:hover {
  color: #28a745;
}

/* Linee divisorie tra le voci di menu */
hr {
  border: 1px solid rgba(255, 255, 255, 0.5);
  margin: 5px 0;
  z-index: 2;
}

/* Stile per gli elementi interni della navbar */
.nav-item {
  padding: 10px 0;
}

.navbar-nav {
  padding: 10px 0;
  list-style: none;
  z-index: 2;
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
