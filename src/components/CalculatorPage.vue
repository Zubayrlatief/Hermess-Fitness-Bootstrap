<template>
    <section id="Calculator">
      <div class="bmi-calculator">
        <h1>BMI Calculator</h1>
        <form @submit.prevent="calculateBMI">
          <div>
            <label for="height">Height (cm):</label>
            <input type="number" v-model="height" id="height" required />
          </div>
          <div>
            <label for="weight">Weight (KG):</label>
            <input type="number" v-model="weight" id="weight" required />
          </div>
          <button type="submit">Calculate</button>
        </form>
        <div v-if="bmi">
          <h2>Your BMI: {{ bmi }}</h2>
          <p>{{ bmiMessage }}</p>
        </div>
  
        <!-- Calorie Calculator -->
        <div class="calorie-calculator">
          <h2>Calorie Calculator</h2>
          <form @submit.prevent="calculateCalories">
            <div>
              <label for="age-calorie">Age:</label>
              <input type="number" v-model="ageForCalories" id="age-calorie" required />
            </div>
            <div>
              <label for="gender-calorie">Gender:</label>
              <select v-model="genderForCalories" id="gender-calorie" required>
                <option value="" disabled>Select Gender</option>
                <option value="male">Male</option>
                <option value="female">Female</option>
              </select>
            </div>
            <div>
              <label for="weight-calorie">Weight (KG):</label>
              <input type="number" v-model="weightForCalories" id="weight-calorie" required />
            </div>
            <div>
              <label for="height-calorie">Height (cm):</label>
              <input type="number" v-model="heightForCalories" id="height-calorie" required />
            </div>
            <div>
              <label for="activity-level">Activity Level:</label>
              <select v-model="activityLevel" id="activity-level" required>
                <option value="" disabled>Select Activity Level</option>
                <option value="sedentary">Sedentary (little or no exercise)</option>
                <option value="light">Lightly active (light exercise/sports 1-3 days/week)</option>
                <option value="moderate">Moderately active (moderate exercise/sports 3-5 days/week)</option>
                <option value="active">Very active (hard exercise/sports 6-7 days a week)</option>
                <option value="extra-active">Extra active (very hard exercise/physical job)</option>
              </select>
            </div>
            <button type="submit">Calculate</button>
          </form>
          <div v-if="calorieNeeds">
            <h3>Your Daily Calorie Needs: {{ calorieNeeds }} kcal</h3>
          </div>
        </div>
  
        <!-- Body Fat Calculator -->
        <div class="body-fat-calculator">
          <h2>Body Fat Calculator</h2>
          <form @submit.prevent="calculateBodyFat">
            <div>
              <label for="age-body-fat">Age:</label>
              <input type="number" v-model="age" id="age-body-fat" required />
            </div>
            <div>
              <label for="gender-body-fat">Gender:</label>
              <select v-model="gender" id="gender-body-fat" required>
                <option value="" disabled>Select Gender</option>
                <option value="male">Male</option>
                <option value="female">Female</option>
              </select>
            </div>
            <div>
              <label for="waist">Waist Circumference (cm):</label>
              <input type="number" v-model="waist" id="waist" required />
            </div>
            <button type="submit">Calculate</button>
          </form>
          <div v-if="bodyFat">
            <h3>Your Body Fat Percentage: {{ bodyFat }}%</h3>
            <p>{{ bodyFatMessage }}</p>
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
        bmiMessage: '',
        // Calorie Calculator Data
        ageForCalories: null,
        genderForCalories: '',
        weightForCalories: null,
        heightForCalories: null,
        activityLevel: '',
        calorieNeeds: null,
        // Body Fat Calculator Data
        age: null,
        gender: '',
        waist: null,
        bodyFat: null,
        bodyFatMessage: ''
      };
    },
    methods: {
      calculateBMI() {
        const heightInMeters = this.height / 100;
        this.bmi = (this.weight / (heightInMeters * heightInMeters)).toFixed(2);
        this.setBMIMessage();
      },
      setBMIMessage() {
        if (this.bmi < 18.5) {
          this.bmiMessage = 'Considered Tiny';
        } else if (this.bmi >= 18.5 && this.bmi < 24.9) {
          this.bmiMessage = 'Considered Average';
        } else if (this.bmi >= 25 && this.bmi < 30) {
          this.bmiMessage = 'Considered Obese';
        } else {
          this.bmiMessage = 'Dangerously Obese';
        }
      },
      calculateCalories() {
        if (!this.ageForCalories || !this.genderForCalories || !this.weightForCalories || !this.heightForCalories || !this.activityLevel) return;
  
        let bmr;
        if (this.genderForCalories === 'male') {
          bmr = 10 * this.weightForCalories + 6.25 * this.heightForCalories - 5 * this.ageForCalories + 5;
        } else if (this.genderForCalories === 'female') {
          bmr = 10 * this.weightForCalories + 6.25 * this.heightForCalories - 5 * this.ageForCalories - 161;
        }
  
        const activityMultiplier = {
          sedentary: 1.2,
          light: 1.375,
          moderate: 1.55,
          active: 1.725,
        };
  
        this.calorieNeeds = (bmr * activityMultiplier[this.activityLevel]).toFixed(2);
      },
      calculateBodyFat() {
        if (!this.age || !this.gender || !this.waist) return;
  
        let bodyFatPercentage;
  
        if (this.gender === 'male') {
          bodyFatPercentage = (1.20 * this.bmi) + (0.23 * this.age) - 16.2;
        } else if (this.gender === 'female') {
          bodyFatPercentage = (1.20 * this.bmi) + (0.23 * this.age) - 5.4;
        }
  
        this.bodyFat = bodyFatPercentage.toFixed(2);
        this.setBodyFatMessage();
      },
      setBodyFatMessage() {
        if (this.gender === 'male') {
          if (this.bodyFat < 6) {
            this.bodyFatMessage = 'Very Low';
          } else if (this.bodyFat >= 6 && this.bodyFat < 24) {
            this.bodyFatMessage = 'Normal';
          } else {
            this.bodyFatMessage = 'High';
          }
        } else if (this.gender === 'female') {
          if (this.bodyFat < 16) {
            this.bodyFatMessage = 'Very Low';
          } else if (this.bodyFat >= 16 && this.bodyFat < 30) {
            this.bodyFatMessage = 'Normal';
          } else {
            this.bodyFatMessage = 'High';
          }
        }
      }
    }
  };
  </script>
  
  <style scoped>
  #Calculator {
    background-color: #050404;
  }
  
  /* Existing Styles for BMI Calculator */
  .bmi-calculator {
    margin-top: 6rem;
    background-color: #967575;
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
  }
  
  </style>