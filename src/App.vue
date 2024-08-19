<template>
   
 <div>
  <NavBar/>
  <LandingPage/>
  <PhilosophyPage/>
  <CarouselSection />
  <ResultsPage/>
  <ConsultationPage/>
  <CalculatorPage/>
  <FooterBottom/>
  <router-view/>
 </div>
 
</template>

<script>
import NavBar from './components/NavBar.vue';
import LandingPage from './components/LandingPage.vue';
import PhilosophyPage from './components/PhilosophyPage.vue';
import ResultsPage from './components/ResultsPage.vue';
import CarouselSection from './components/CarouselSection.vue';
import ConsultationPage from './components/ConsultationPage.vue';
import CalculatorPage from './components/CalculatorPage.vue';
import FooterBottom from './components/FooterBottom.vue';

export default {
  components:{
    NavBar,
    LandingPage,
    PhilosophyPage,
    ResultsPage,
    CarouselSection,
    ConsultationPage,
    CalculatorPage,
    FooterBottom,
  }
};

</script>


<style>
.div{

}
</style>
