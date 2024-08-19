<template>
  <section id="carousel-section" class="my-5">
    <h1 class="h1-text">REAL RESULTS</h1>
    <div class="autoShow">
      <!-- Carousel 1 -->
      <div id="carouselExample1" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-indicators">
          <button type="button" data-bs-target="#carouselExample1" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
          <button type="button" data-bs-target="#carouselExample1" data-bs-slide-to="1" aria-label="Slide 2"></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="https://zubayrlatief.github.io/hosted-images/295c0d98-6739-4b40-97e2-433db661ff9e.JPG" class="d-block w-100" alt="Slide 1">
          </div>
          <div class="carousel-item">
            <img src="https://zubayrlatief.github.io/hosted-images/4f89ff2d-eee2-488b-97f7-74ea3d33d73d.JPG" class="d-block w-100" alt="Slide 2">
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample1" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExample1" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>

      <!-- Carousel 2 -->
      <div id="carouselExample2" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-indicators">
          <button type="button" data-bs-target="#carouselExample2" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
          <button type="button" data-bs-target="#carouselExample2" data-bs-slide-to="1" aria-label="Slide 2"></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="https://zubayrlatief.github.io/hosted-images/8975fc3f-250f-4284-b5e2-74e76bcb9e1a.JPG" class="d-block w-100" alt="Slide 1">
          </div>
          <div class="carousel-item">
            <img src="https://zubayrlatief.github.io/hosted-images/07a7d979-94b1-4bd5-9e5b-575fa0cf6edf.JPG" class="d-block w-100" alt="Slide 2">
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample2" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExample2" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>

      <!-- Carousel 3 -->
      <div id="carouselExample3" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-indicators">
          <button type="button" data-bs-target="#carouselExample3" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
          <button type="button" data-bs-target="#carouselExample3" data-bs-slide-to="1" aria-label="Slide 2"></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="https://via.placeholder.com/800x400" class="d-block w-100" alt="Slide 1">
          </div>
          <div class="carousel-item">
            <img src="https://via.placeholder.com/800x400" class="d-block w-100" alt="Slide 2">
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample3" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExample3" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>

    </div>
  </section>
</template>

<script>
export default {
  name: 'CarouselSection'
};
</script>

<style scoped>
#carousel-section {
  background-color: black;
  padding: 0;
  margin: 0;
  width: 100%; /* Ensure it spans the full width */
}
.my-5 {
  margin-top: -2rem !important;
  margin-bottom: -2rem !important;
}

.h1-text{
    border: 2px rgb(29, 25, 25) solid;
    color: rgb(193, 189, 185);
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0.75rem;
    font-style: italic;

}

.carousel-item{
  margin: 2rem;
}
/* Auto Show Animation */
.autoShow {
    display: flex;
    align-items: center;
    margin-bottom: 2rem;
    animation: autoShowAnimation both;
    animation-timeline: view(100% 1%);
}

@keyframes autoShowAnimation {
    from {
        opacity: 0;
        transform: translateY(200px) scale(0.3);
    }
    to {
        opacity: 1;
        transform: translateY(0) scale(1);
    }
}

.h1-text{
    animation: autoShowAnimation both;
    animation-timeline: view(10% 50%);
}

@keyframes autoShowAnimation {
    from {
        opacity: 0;
        transform: translateY(200px) scale(0.3);
    }
    to {
        opacity: 1;
        transform: translateY(0) scale(1);
    }
}

</style>

