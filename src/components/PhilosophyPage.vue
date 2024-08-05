<template>
    <section id="Philosohy">
        <div class="container-main">
            <div class="cointainer-card">
                <div class="card-text">
                    <p class="card-p-text">Hover Me</p>
                    <div class="card-countent">
                        <p>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque hic soluta amet, ipsum quia
                            numquam excepturi veritatis deleniti similique ipsam obcaecati nulla dolor, sapiente earum
                            blanditiis pariatur minima iure repudiandae.
                        </p>
                    </div>
                </div>
                <div class="container-bmi-calc">

                </div>
            </div>
        </div>
    </section>
</template>
<script>
export default {

}
</script>
<style>
#Philosophy {
    background-color: black;
    display: flex;
    flex-direction: row;
}

.container-main {
    display: flex;
    flex-direction: column;
    height: 100vh;
}

.container-card {}

.container-bmi-calc {}

/* card */
.card-text {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    position: relative;
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
</style>