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

#Calculator{
    background-color: #212121;
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

</style>