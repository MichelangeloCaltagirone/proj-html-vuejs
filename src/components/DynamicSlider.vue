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
  
    <!-- SEZIONE CERTIFICATI -->
     <div id="section-certificates-wrapper">
        <h3>
            Start today for getting <mark>Online Certification</mark>
        </h3>
        <h2>
          You can be your own guiding star with our help!
        </h2>
        <div class="button-container d-flex justify-content-center">
          <button>
            Get started now
          </button>
        </div>
     </div>
  </template>
  
  <style lang="scss" scoped>
  * {
    font-family: 'Roboto';
  }
  
  // Carousel title
  
  .carousel-title h3 {
    margin-top: 115px;
    font-size: 15px;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 2px;
    color: #8C89A2;
  }
  
  .carousel-title h2 {
    font-weight: 34px;
    color: #3F3A64;
  }
  
  .carousel-title mark {
    font-weight: 400;
    color: rgb(83, 170, 151);
    margin: 0;
    background-color: transparent;
  }
  
  // CAROUSEL
  #customCarousel{
    max-width: 60%;
    margin: 0 auto;
  }
  
  .carousel-inner {
    transition: transform 0.8s ease-in-out; /* Transizione smooth */
  }
  
  .custom-carousel-card {
    margin-top: 50px;
    width: 700px;
    height: 350px;
    border: 1px solid lightgray;
    padding: 40px;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1); /* Aggiunta ombra */
  }
  
  .custom-carousel-card .custom-title {
    font-size: 20px;
    color: #3F3A64;
    text-align: left;
  }
  
  .custom-carousel-card .custom-text {
    margin-top: 25px;
    margin-bottom: 25px;
    font-size: 18px;
    font-weight: 500;
    color: #696969;
    white-space: pre-line;
    text-align: left;
  }
  
  .custom-carousel-card img {
    height: 70px;
    width: 70px;
    max-width: 100%;
    border-radius: 50%;
  }
  
  .custom-img-wrapper {
    display: flex;
    align-items: center;
  }
  
  .custom-carousel-img-content {
    margin-left: 25px;
    flex-direction: column;
    align-items: start;
    justify-content: center;
  }
  
  .custom-carousel-img-content .custom-img-title {
    font-size: 15px;
    color: #3F3A64;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 12px;
  }
  
  .custom-carousel-img-content .custom-img-text {
    font-size: 14px;
    color: #7e7e7e;
    margin-bottom: 0;
  }
  
  // SEZIONE CERTIFICATI
  #section-certificates-wrapper{
    margin: 60px auto;
  }
  
  #section-certificates-wrapper h3{
    margin-bottom: 0;
    font-size: 24px;
    font-weight: 700;
    color: #3F3A64;
  }
  
  #section-certificates-wrapper h2{
    font-weight: 700;
    font-size: 34px;
    color: #3F3A64;
  }
  
  #section-certificates-wrapper mark{
    font-weight: 400;
    color: rgb(83, 170, 151);
    margin: 0;
    background-color: transparent;
  }
  
  #section-certificates-wrapper button{
    margin-top: 15px;
    min-height: 52px;
    width: 260px;
    background-color: rgb(83, 170, 151);
    color: white;
  }
  
  #section-certificates-wrapper button:hover{
    cursor: pointer;
    background-color: rgb(127, 205, 188);
  }
  
  #section-certificates-wrapper button:active{
    cursor: pointer;
    background-color: rgb(83, 170, 151);
  }
  </style>