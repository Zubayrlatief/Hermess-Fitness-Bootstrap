<!-- make this a page with a big transform button -->
<!-- page shows the aestetics program and the weight loss program
  and the musle building program -->
<!-- the card must be animated wher it lights up when you hover -->
<template>
    <section id="Consultation">
    <div class="autoShow">
        
    <h1 class="h1-text">CHANGE WITH US</h1>
        <div class="container-cards">
            <div class="card">
                <div><img src=""></div>
            </div>
            <div class="card">
                <div><img src=""></div>
            </div>
            <div class="card">
                <div><img src=""></div>
            </div>
        </div>
        <div class="container-button">
                <h1 class="h1">Take the initiative and tranform your life</h1>
                    <button class="Btn">Click Me</button> 
        </div>
    </div>
    </section>

</template>
<script>
export default {

}
</script>
<style scoped>

#Consultation{
    background-color: black;
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

/* Container */
.container-cards{
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    padding: 4rem;
}

/* Cards */
.card {
 width: 40%;
 height: 254px;
 box-shadow: 0 10px 10px rgba(116, 98, 98, 0.212);
 background: #423838;
 display: flex;
 border-radius: 20px;
 justify-content: center;
 position: relative;
 transition: all .4s;
 margin: 1.25rem;
}

.card::before {
 content: '---content---';
 letter-spacing: 0.2em;
 position: absolute;
 bottom: 8px;
 left: 20px;
 color: rgb(51, 51, 51);
 font-size: 0.8em;
 font-weight: 700;
}

.card div {
 width: 100%;
 height: 100%;
 border-radius: 20px;
 box-shadow: 0 0 10px rgba(0, 0, 0, 0.212);
 cursor: pointer;
 z-index: 10;
 transition: all .4s;
 background-color: #474141;
}

.card:hover div {
 transform: translateY(-30px);
}

 /* button */
 .container-button{
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: center;
    flex-direction: column;
    padding-bottom: 2rem;
    
 }
.Btn {
 margin: 2rem;
  width: 150px;
  height: 50px;
  background-color: transparent;
  color: white;
  font-weight: bold;
  border-width: 2px;
  border-color: #FF5858;
  border-radius: 20px;
  transition: all 0.3s;
}

.Btn:hover {
  transform: translateY(-10px);
  background-color: #FF5858;
}

.Btn::after {
  transform: translateY(0);
}

/* autoshow animation */
.autoShow {
    margin-bottom: 2rem;
    animation: autoShowAnimation both;
    animation-timeline: view(90% 5%);
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