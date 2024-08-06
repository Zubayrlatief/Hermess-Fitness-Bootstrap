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
</template>

<script>
import NavBar from './components/NavBar.vue';
import ConsultationPage from './components/ConsultationPage.vue';
import LandingPage from './components/LandingPage.vue';
import PhilosophyPage from './components/PhilosophyPage.vue';
import ResultsPage from './components/ResultsPage.vue';
import FooterBottom from './components/FooterBottom.vue';
import CalculatorPage from './components/CalculatorPage.vue';
export default {
  components:{
    NavBar,
    LandingPage,
    PhilosophyPage,
    ResultsPage,
    CalculatorPage,
    ConsultationPage,
    FooterBottom,
  }
}
</script>


<style>

</style>
