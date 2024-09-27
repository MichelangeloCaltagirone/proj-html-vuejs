<template>
    <div class="carousel-container">
      <div class="carousel-title">
        <h3>Great words about MaxCoach</h3>
        <h2>Our <mark>top learners'</mark>verbatim</h2>
      </div>
      
      <!-- Carosello con 4 slide -->
      <div id="customCarousel" class="carousel slide" data-bs-ride="carousel">
        <!-- Indicatori per ciascuna slide -->
        <div class="carousel-indicators">
          <button type="button" data-bs-target="#customCarousel" data-bs-slide-to="0" class="active" aria-current="true"></button>
          <button type="button" data-bs-target="#customCarousel" data-bs-slide-to="1"></button>
          <button type="button" data-bs-target="#customCarousel" data-bs-slide-to="2"></button>
          <button type="button" data-bs-target="#customCarousel" data-bs-slide-to="3"></button>
        </div>
  
        <!-- Slide -->
        <div class="carousel-inner">
          <div class="carousel-item active">
            <div class="custom-carousel-card">
              <h4 class="custom-title">High level of efficiency and scientific teaching methods</h4>
              <p class="custom-text">
                I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.
              </p>
              <div class="custom-img-wrapper d-flex justify-content-start align-items-center">
                <img src="../assets/img/testimonial-avata-02.jpg" alt="testimonial-avatar-01">
                <div class="custom-carousel-img-content d-flex">
                  <h6 class="custom-img-title">Mina Hollace</h6>
                  <p class="custom-img-text">/ Freelancer</p>
                </div>
              </div>
            </div>
          </div>
  
          <div class="carousel-item">
            <div class="custom-carousel-card">
              <h4 class="custom-title">Professional team of specialists and passionate mentors at reach</h4>
              <p class="custom-text">
                I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.
              </p>
              <div class="custom-img-wrapper d-flex justify-content-start align-items-center">
                <img src="../assets/img/testimonial-avata-01.jpg" alt="testimonial-avatar-02">
                <div class="custom-carousel-img-content d-flex">
                  <h6 class="custom-img-title">Madley Pondor</h6>
                  <p class="custom-img-text">/ IT Specialist</p>
                </div>
              </div>
            </div>
          </div>
  
          <div class="carousel-item">
            <div class="custom-carousel-card">
              <h4 class="custom-title">It's a choice of quality for people with special needs</h4>
              <p class="custom-text">
                I'm a very strict person so I require everything to be organized and neat. Then, I'll be able to make things right and shine. MaxCoach guys just got me.
              </p>
              <div class="custom-img-wrapper d-flex justify-content-start align-items-center">
                <img src="../assets/img/testimonial-avata-03.jpg" alt="testimonial-avatar-03">
                <div class="custom-carousel-img-content d-flex">
                  <h6 class="custom-img-title">Florence Themes</h6>
                  <p class="custom-img-text">/ Multimedia Admin</p>
                </div>
              </div>
            </div>
          </div>
  
          <div class="carousel-item">
            <div class="custom-carousel-card">
              <h4 class="custom-title">I am proud of MaxCoach</h4>
              <p class="custom-text">
                The team at MaxCoach is simply outstanding. They helped me achieve all my goals in a timely and professional manner. Highly recommended.
              </p>
              <div class="custom-img-wrapper d-flex justify-content-start align-items-center">
                <img src="../assets/img/testimonial-avata-04.jpg" alt="testimonial-avatar-04">
                <div class="custom-carousel-img-content d-flex">
                  <h6 class="custom-img-title">John Doe</h6>
                  <p class="custom-img-text">/ CEO</p>
                </div>
              </div>
            </div>
          </div>
        </div>
  
        <!-- Pulsanti invisibili per spostarsi tra le slide -->
        <button class="carousel-control-prev" type="button" data-bs-target="#customCarousel" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#customCarousel" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </div>
  