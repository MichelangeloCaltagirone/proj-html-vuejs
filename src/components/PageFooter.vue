<template>
  <footer class="bg-light py-5">
    <div class="container">
      <div class="row">
        <div class="col-lg-4 col-md-12 col-12 mb-4">
          <h5 class="footer-title">Address</h5>
          <ul class="list-unstyled">
            <li>382 NE 191st St # 87394 Miami, FL 33179-3899</li>
            <li>+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)</li>
            <li><a href="#" class="footer-link">support@maxcoach.com</a></li>
            <div>
              <a href="#" class="social-icon"><i class="fa-brands fa-facebook-f"></i></a>
              <a href="#" class="social-icon"><i class="fa-brands fa-twitter"></i></a>
              <a href="#" class="social-icon"><i class="fa-brands fa-instagram"></i></a>
              <a href="#" class="social-icon"><i class="fa-brands fa-linkedin-in"></i></a>
            </div>
          </ul>
        </div>

        <div class="col-lg-4 col-md-6 col-12 mb-4">
          <h5 class="footer-title">Explore</h5>
          <ul class="list-unstyled">
            <li><a href="#" class="footer-link">Start here</a></li>
            <li><a href="#" class="footer-link">Blog</a></li>
            <li><a href="#" class="footer-link">About Us</a></li>
            <li><a href="#" class="footer-link">Success story</a></li>
            <li><a href="#" class="footer-link">Courses</a></li>
            <li><a href="#" class="footer-link">Contact us</a></li>
          </ul>
        </div>

        <div class="col-lg-4 col-md-6 col-12 mb-4">
          <h5 class="footer-title">Information</h5>
          <ul class="list-unstyled">
            <li><a href="#" class="footer-link">Membership</a></li>
            <li><a href="#" class="footer-link">Purchase</a></li>
            <li><a href="#" class="footer-link">Privacy policy</a></li>
            <li><a href="#" class="footer-link">Terms of services</a></li>
            <li><a href="#" class="footer-link">Courses</a></li>
            <li><a href="#" class="footer-link">Contact us</a></li>
          </ul>
        </div>
      </div>

      <div class="text-center mt-4">
        <p class="mb-0">&copy; {{ new Date().getFullYear() }} MaxCoach. All Rights Reserved.</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped>
.footer-title {
  font-weight: bold;
  margin-bottom: 1rem;
}

.footer-link {
  color: #333;
  text-decoration: none;
}

.footer-link:hover {
  text-decoration: underline;
}

.social-icon {
  margin: 0 10px;
  font-size: 1.5rem;
  color: #333;
}

.social-icon:hover {
  color: #28a745;
}
</style>
