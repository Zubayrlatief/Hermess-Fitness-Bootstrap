<template>
   
 <div>
  <NavBar/>
  <LandingPage/>
  <PhilosophyPage/>
  <ResultsPage/>
  <CalculatorPage/>
  <ConsultationPage/>
  <FooterBottom/>
  <router-view/>
 </div>
 <div id="app">
    <CarouselSection />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue';
import LandingPage from './components/LandingPage.vue';
import PhilosophyPage from './components/PhilosophyPage.vue';
import ResultsPage from './components/ResultsPage.vue';
import CarouselSection from './components/CarouselSection.vue';
import CalculatorPage from './components/CalculatorPage.vue';
import ConsultationPage from './components/ConsultationPage.vue';
import FooterBottom from './components/FooterBottom.vue';

export default {
  components:{
    NavBar,
    LandingPage,
    PhilosophyPage,
    ResultsPage,
    CarouselSection,
    CalculatorPage,
    ConsultationPage,
    FooterBottom,
  }
};

</script>


<style>

</style>
