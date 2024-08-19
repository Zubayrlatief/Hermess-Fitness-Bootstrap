<template>
<nav class="navbar navbar-expand-lg fixed-top ">
  <div class="container justify-content-center">
    <a class="navbar-brand" href="#Landing"><img class="logo" src="https://zubayrlatief.github.io/hosted-images/hermessfitnesslogo.png"></a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse flex-grow-0" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
         <a class="nav-link active text-white" aria-current="page" href="Philosophy">Philosophy</a>
        </li>
        <li class="nav-item">
         <a class="nav-link text-white" href="carousel-section">Results</a>
        </li>
        <li class="nav-item">
         <a class="nav-link text-white" href="Consultation">Consultation</a>
        </li>
       </ul>
      </div>
    </div>

</nav> 
</template>
<script>
export default {
  name: 'NavBar',
  props: {
  }
}
</script>

<style scoped>
.navbar{
  background-color: #040404;
}
.navlink{
  color: white;
  background-color: aliceblue;
  text-decoration-color: white;
}
.logo{
  width: 4.5rem;
  height: 4.25rem;
}
</style>
