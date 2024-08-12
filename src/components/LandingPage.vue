<template>
    <section id="landing">
        <div class="container-page">
            <img class="landing-image" src="https://zubayrlatief.github.io/hosted-images/IMG_2337.jpg" alt="image">
            <button class="batman" >
  <span >TRANSFORM</span>
</button>
            <div class="card">
                <p><span>calorie calc</span></p>
                <p><span>total calc</span></p>
                <p><span>bmi calc</span></p>
            </div>
        </div>
    </section>
</template>
<script>
export default {

}
</script>
<style scoped>
.landing {
    background-color: #040404;
    max-width: 100%;
    display: flex;
    justify-content: center;
    flex-direction: row;
    margin: 0;
    padding: 0;
}

.landing-image {
    width: 30%;
    height: auto;
    max-height: 700px; /* Adjusted to keep a moderate size */
    margin-left: 2rem;
    margin-top: 1rem; /* Slightly reduced */
}

/* Whole page */
.container-page {
    background-color: #040404;
    display: flex;
    justify-content: center;
    flex-direction: row;
    padding: 1rem; /* Slightly reduced padding */
    margin: 0;
}


/* Card */
.card {
    width: 25%; /* Slightly larger width */
    max-width: 35%;
    height: auto;
    max-height: 700px; /* Adjusted for a moderate height */
    border-radius: 4px;
    background: #212121;
    display: flex;
    flex-direction: column;
    gap: 5px;
    padding: 0.5rem; /* Added some padding for spacing */
    margin: 0 auto;
}

.card p {
    height: 100%;
    flex: 1;
    overflow: hidden;
    cursor: pointer;
    border-radius: 2px;
    transition: all .5s;
    background: #212121;
    border: 1px solid #ff5a91;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0;
}

.card p span {
    min-width: 12em; /* Slightly larger min-width */
    padding: .5em;
    text-align: center;
    transform: rotate(-90deg);
    transition: all .5s;
    text-transform: uppercase;
    color: #ff568e;
    letter-spacing: .1em;
}

.card p:hover {
    flex: 4;
}

.card p:hover span {
    transform: rotate(0);
}

/* Responsive Styles */
@media (max-width: 768px) {
    .card {
        width: 100%;
        height: auto;
        flex-direction: column;
    }

    .card p {
        width: 100%;
        height: auto;
    }

    .card p span {
        transform: rotate(0);
        min-width: 0;
        width: 100%;
        padding: 1em 0;
    }

    .card p:hover {
        flex: 1;
    }
}


/* button */

.batman{
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: center;
}
button {
 border: none;
 position: relative;
 width: 200px;
 height: 73px;
 padding: 0;
 z-index: 2;
 -webkit-mask: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' height='868' width='2500' viewBox='0 0 726 252.17'%3E%3Cpath d='M483.92 0S481.38 24.71 466 40.11c-11.74 11.74-24.09 12.66-40.26 15.07-9.42 1.41-29.7 3.77-34.81-.79-2.37-2.11-3-21-3.22-27.62-.21-6.92-1.36-16.52-2.82-18-.75 3.06-2.49 11.53-3.09 13.61S378.49 34.3 378 36a85.13 85.13 0 0 0-30.09 0c-.46-1.67-3.17-11.48-3.77-13.56s-2.34-10.55-3.09-13.61c-1.45 1.45-2.61 11.05-2.82 18-.21 6.67-.84 25.51-3.22 27.62-5.11 4.56-25.38 2.2-34.8.79-16.16-2.47-28.51-3.39-40.21-15.13C244.57 24.71 242 0 242 0H0s69.52 22.74 97.52 68.59c16.56 27.11 14.14 58.49 9.92 74.73C170 140 221.46 140 273 158.57c69.23 24.93 83.2 76.19 90 93.6 6.77-17.41 20.75-68.67 90-93.6 51.54-18.56 103-18.59 165.56-15.25-4.21-16.24-6.63-47.62 9.93-74.73C656.43 22.74 726 0 726 0z'/%3E%3C/svg%3E") no-repeat 50% 50%;
 mask: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' height='868' width='2500' viewBox='0 0 726 252.17'%3E%3Cpath d='M483.92 0S481.38 24.71 466 40.11c-11.74 11.74-24.09 12.66-40.26 15.07-9.42 1.41-29.7 3.77-34.81-.79-2.37-2.11-3-21-3.22-27.62-.21-6.92-1.36-16.52-2.82-18-.75 3.06-2.49 11.53-3.09 13.61S378.49 34.3 378 36a85.13 85.13 0 0 0-30.09 0c-.46-1.67-3.17-11.48-3.77-13.56s-2.34-10.55-3.09-13.61c-1.45 1.45-2.61 11.05-2.82 18-.21 6.67-.84 25.51-3.22 27.62-5.11 4.56-25.38 2.2-34.8.79-16.16-2.47-28.51-3.39-40.21-15.13C244.57 24.71 242 0 242 0H0s69.52 22.74 97.52 68.59c16.56 27.11 14.14 58.49 9.92 74.73C170 140 221.46 140 273 158.57c69.23 24.93 83.2 76.19 90 93.6 6.77-17.41 20.75-68.67 90-93.6 51.54-18.56 103-18.59 165.56-15.25-4.21-16.24-6.63-47.62 9.93-74.73C656.43 22.74 726 0 726 0z'/%3E%3C/svg%3E") no-repeat 50% 50%;
 -webkit-mask-size: 100%;
 cursor: pointer;
 background-color: white;
 transform: translateY(8px)
}

button:after {
 content: '';
 position: absolute;
 left: 0;
 right: 0;
 bottom: 0;
 box-shadow: 0px 0 0 0 white;
 transition: all 2s ease;
}

button:hover:after {
 box-shadow: 0px -13px 56px 12px #ffffffa6;
}

button span {
 position: absolute;
 width: 100%;
 font-size: 15px;
 font-weight: 100;
 left: 50%;
 top: 39%;
 letter-spacing: 3px;
 text-align: center;
 transform: translate(-50%,-50%);
 color: black;
 transition: all 2s ease;
}

button:hover span {
 color: white;
}

button:before {
 content: '';
 position: absolute;
 width: 0;
 height: 100%;
 background-color: black;
 left: 50%;
 top: 50%;
 transform: translate(-50%, -50%);
 transition: all 1s ease;
}

button:hover:before {
 width: 100%;
}



</style>