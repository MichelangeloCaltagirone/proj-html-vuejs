<template>
  <div class="sidebar" v-if="isVisible">
    <!-- Header della Sidebar -->
    <div class="sidebar-header">
      <img src="../assets/images/dark-logo.png" alt="Logo" class="logo" />
      <button class="btn-close" @mouseover="hoverClose" @mouseleave="leaveClose" @click="toggleSidebar">
        <img src="../assets/images/close.svg" alt="Close" />
      </button>
    </div>

    <!-- Navbar -->
    <ul class="navbar-nav">
      <li v-for="(item, index) in menuItems" :key="index" class="nav-item">
        <div class="nav-link" @click="toggleDropdown(item)">
          {{ item.name }}
          <span class="dropdown-arrow" v-if="item.submenu">▼</span>
        </div>
        <ul v-if="item.isOpen" class="dropdown-menu">
          <li v-for="(subItem, subIndex) in item.submenu" :key="subIndex" class="dropdown-item">
            {{ subItem.name }}
          </li>
        </ul>
        <hr v-if="index < menuItems.length - 1" /> <!-- Linea divisoria -->
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    menuItems: Array,
    isVisible: Boolean,
  },
  data() {
    return {
      closeIcon: '../assets/images/close-icon.png',
      isHovered: false,
    };
  },
  methods: {
    toggleSidebar() {
      this.$emit('close-sidebar');
    },
    toggleDropdown(item) {
      // Chiude gli altri dropdown se aperti
      this.menuItems.forEach(i => {
        if (i !== item) i.isOpen = false; // Chiudi altri dropdown
      });
      item.isOpen = !item.isOpen; // Inverti lo stato del dropdown cliccato
    },
  },
};
</script>

<style scoped>
.sidebar {
  position: fixed;
  top: 0;
  right: 0;
  width: 300px;
  height: 100%;
  background-color: #fff;
  box-shadow: -2px 0 5px rgba(0, 0, 0, 0.1);
  z-index: 1050;
  padding: 20px;
  transition: transform 0.3s ease;
  overflow-y: auto;
  background-image: url('../assets/images/mobile-bg.jpg');
  background-size: cover;
  background-position: center;
}

.sidebar:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgb(78, 72, 110, 0.7);
  z-index: 1;
}

.sidebar .btn-close {
  position: absolute;
  top: 10px;
  right: 10px;
  font-size: 20px;
  border: none;
  background: none;
  z-index: 2;
}

.navbar-nav .nav-item .nav-link {
  padding: 10px;
  color: #000;
  text-decoration: none;
  display: block;
  transition: color 0.3s ease;
  z-index: 2;
  color: #fff;
}

.logo {
  height: 30px;
}

.btn-close {
  background: none;
  border: none;
  cursor: pointer;
  transition: opacity 0.3s;
}

.btn-close img {
  width: 30px;
}

.btn-close:hover {
  opacity: 0.7;
}

.nav-item {
  padding: 10px 0;
}

.navbar-nav {
  padding: 10px 0;
  list-style: none;
}

.nav-link {
  color: #fff;
  /* Colore del testo dei link */
  text-decoration: none;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.dropdown-menu {
  background-color: rgba(255, 255, 255, 0.8);
  padding: 10px;
  border-radius: 5px;
}

.dropdown-item {
  color: black;
  padding: 5px 0;
}

hr {
  border: 1px solid white;
  margin: 5px 0;
}

.dropdown-arrow {
  margin-left: 5px;
  /* Spazio tra il nome e l'icona della freccia */
}
</style>
