<template>
    <section id="Philosohy">
           <div class="text-card">
              <div class="bmi-card">
               
                <div class="bmi-calculator">
                    <h1>BMI Calculator</h1>
                    <form @submit.prevent="calculateBMI">
                        <div>
                            <label for="height">Height (cm):</label>
                            <input type="number" v-model="height" id="height" required />
                        </div>
                        <div>
                            <label for="weight">Weight in (KG)</label>
                            <input type="number" v-model="weight" id="weight" required />
                        </div>
                        <button type="submit">Calculate</button>
                    </form>
                    <div v-if="bmi">
                        <h2>Your BMI {{ bmi }}</h2>
                        <p>{{ bmiMessage }}</p>
                    </div>
 
                </div>
                                
<div class="container">
  <div class="card1"></div>
  <div class="card2"></div>
  <div class="card3">
     <h1 class="text">
                    Our main goal for our clinets<br>
                    is to make them succed in progressive,<br>
                    incremental and substantaialsteps </h1>
  </div>
</div>

            </div>
        </div>
    </section>
</template>
<script>
export default {
    data() {
        return {
            height: null,
            weight: null,
            bmi: null,
            bmiMessage: ''
        };
    },
    methods: {
        calculateBMI() {
            const heightInMeters = this.height / 100
            this.bmi = (this.weight / (heightInMeters * heightInMeters)).toFixed(2);
            this.setBMIMessage();
        },
        setBMIMessage() {
            if (this.bmi < 18.5) {
                this.bmiMessage = 'Considered Tiny';
            } else if (this.bmi >= 18.5 && this.bmi < 24.9) {
                this.bmiMessage = 'Considered Average';
            } else if (this.bmi >= 25 && this.bmi < 30) {
                this.bmiMessage = 'Considered Obese'
            } else {
                this.bmiMessage = 'Dangerously Obese';
            }
        }
    }
};


</script>
<style scoped>
/* move to bottom */
#Philosophy {
    background-color: #040404;


}

.container-card {
    margin-left: 8rem;
    display: flex;
    flex-direction: row;
    align-content: space-between;

}

.bmi-card {
    background-color: #040404;
    display: flex;
    flex-direction: row;
    align-content: space-between;

}

/* card */
.card-text {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 300px;
    height: 350px;
    border-radius: 6px;
    transition: .3s;
    background-color: #000;
}

.card-p-text {
    position: absolute;
    text-align: center;
}

.card-text::after {
    content: "";
    position: absolute;
    z-index: -6;
    border-radius: 6px;
    width: 320px;
    height: 370px;
    background-color: #8EC5FC;
    transition: .7s;
    background-image: linear-gradient(62deg, #8EC5FC 0%, #E0C3FC 100%);
}

.card-countent {
    padding: 20px;
    text-align: center;
    color: transparent;
    transition: all .7s;
    opacity: 0;
}

.card-text:hover {
    transition: .7s;
    transform: rotate(180deg);
}

.card-text:hover>.card-p {
    color: transparent;
}

.card-text:hover>.card-countent {
    opacity: 1;
    color: #000;
    transform: rotate(-180deg);
}

/* bmi calc */
.bmi-calculator {
    margin-top: 6rem;
    background-color: #212121;
    max-width: 400px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ff5a91;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.bmi-calculator h1 {
    text-align: center;
    color: #ccc;
}

.bmi-calculator form {
    display: flex;
    flex-direction: column;
}

.bmi-calculator form div {
    margin-bottom: 10px;
}

.bmi-calculator label {
    margin-bottom: 5px;
    font-weight: bold;
    color: #ccc;
}

.bmi-calculator input {
    padding: 8px;
    font-size: 16px;
    border: 1px solid #ccc;
    border-radius: 4px;
}

.bmi-calculator button {
    padding: 10px;
    font-size: 16px;
    color: #fff;
    background-color: #111213;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

.bmi-calculator button:hover {
    background-color: #1e2022;
}

.bmi-calculator h2 {
    text-align: center;
    margin-top: 20px;
    color: #ff5a91;
}

.bmi-calculator p {
    text-align: center;
    font-weight: bold;
    color: #ff5a91;
}
/* card-for-text */
 
.container {
  position: relative;
 margin-top: 8rem;
  width: 360px;
}

.container > * {
  width: 340px;
  height: 120px;
  border: solid 1px #bebebe;
  background-color: #1f1f1f;
  position: absolute;
  border-radius: 10px;
  padding: 10px;
  color: #fff;
  box-shadow: 0px 8px 20px -10px #bbbbbb;
  text-shadow: 0px 0px 5px #fff;
  letter-spacing: 1px;
  background-image: radial-gradient(circle 160px at 50% 120%, #353535, #1f1f1f);
}

.card1 {
  width: 300px;
  margin: -20px 0px 0px 20px;
}
.card2 {
  width: 320px;
  margin: -10px 0px 0px 10px;
}

.text{
    font-size: large;
    display: flex;
    justify-content: center;
    align-items: center;
}

</style>