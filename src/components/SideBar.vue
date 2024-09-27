<template>
  <div v-if="isVisible" class="sidebar">
    <button class="btn-close" @click="$emit('close-sidebar')">X</button>
    <ul class="navbar-nav">
      <li v-for="(item, index) in menuItems" :key="index" class="nav-item">
        <a class="nav-link" :href="item.link">{{ item.name }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Sidebar',
  props: {
    isVisible: {
      type: Boolean,
      required: true,
    },
    menuItems: {
      type: Array,
      required: true,
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
  color: #fff;
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
}

.navbar-nav .nav-item .nav-link:hover {
  color: #007bff;
}
</style>
