<template>
    <section id="landing">
        <div class="container-page">
            <img class="landing-image" src="https://zubayrlatief.github.io/hosted-images/IMG_2337.jpg" alt="image">
            <div class="card">
                <p><span>calorie calc</span></p>
                <p><span>total calc</span></p>
                <p><span>bmi calc</span></p>
            </div>
            <div class="mid">
            <button class="btn-12"><span>TRANSFORM</span></button>
            <h2 class="text-1">TRANFORM YOUR LIFE</h2>
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
    width: 25%;
    height: auto;
    max-height: 700px; /* Adjusted to keep a moderate size */
    margin-right: 10%;
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

.text-1{
    display: flex;
    justify-content: center;
    justify-items: center;
    color: #827f80;
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
}

.card p {
    height: 100%;
    flex: 1;
    overflow: hidden;
    cursor: pointer;
    border-radius: 2px;
    transition: all .5s;
    background: #212121;
    border: 1px solid #b4393984;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0;
}

.card p span {
    min-width: 12em; /* Slightly larger min-width */
    padding-left: 0.5em;
    text-align: center;
    transform: rotate(-90deg);
    transition: all .5s;
    text-transform: uppercase;
    color: #c51e1e84;;
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

    .mid{
      max-width: 50%;
    }
}

/* mid */
.mid{
    margin-left: 10%;
    margin-top: 20%;
}

/* button class */ 
.btn-12,
.btn-12 *,
.btn-12 :after,
.btn-12 :before,
.btn-12:after,
.btn-12:before {
  border: 0 solid;
  box-sizing: border-box;
}

.btn-12 {
  -webkit-tap-highlight-color: transparent;
  -webkit-appearance: button;
  background-color: #000;
  background-image: none;
  color: #fff;
  cursor: pointer;
  font-family: ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont,
    Segoe UI, Roboto, Helvetica Neue, Arial, Noto Sans, sans-serif,
    Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  font-size: 100%;
  font-weight: 900;
  line-height: 1.5;
  margin: 0;
  -webkit-mask-image: -webkit-radial-gradient(#000, #fff);
  padding: 0;
  text-transform: uppercase;
  border-radius: 99rem;
  border-width: 2px;
  overflow: hidden;
  padding: 0.8rem 3rem;
  position: relative;
}

.btn-12:disabled {
  cursor: default;
}

.btn-12:-moz-focusring {
  outline: auto;
}

.btn-12 svg {
  display: block;
  vertical-align: middle;
}

.btn-12 [hidden] {
  display: none;
}

.btn-12 span {
  mix-blend-mode: difference;
}

.btn-12:after,
.btn-12:before {
  background: linear-gradient(
    90deg,
    #fff 25%,
    transparent 0,
    transparent 50%,
    #fff 0,
    #fff 75%,
    transparent 0
  );
  content: "";
  inset: 0;
  position: absolute;
  transform: translateY(var(--progress, 100%));
  transition: transform 0.2s ease;
}

.btn-12:after {
  --progress: -100%;
  background: linear-gradient(
    90deg,
    transparent 0,
    transparent 25%,
    #fff 0,
    #fff 50%,
    transparent 0,
    transparent 75%,
    #fff 0
  );
  z-index: -1;
}

.btn-12:hover:after,
.btn-12:hover:before {
  --progress: 0;
}

/* Media Queries for Responsiveness */

/* Smaller screens (tablets, mobile devices) */
@media (max-width: 1024px) {
  .btn-12 {
    font-size: 90%;
    padding: 0.6rem 2.5rem;
  }
}

/* Even smaller screens (phones) */
@media (max-width: 768px) {
  .btn-12 {
    font-size: 80%;
    padding: 0.5rem 2rem;
  }
}

/* Very small screens (small phones) */
@media (max-width: 480px) {
  .btn-12 {
    font-size: 70%;
    padding: 0.4rem 1.5rem;
  }
}


</style>