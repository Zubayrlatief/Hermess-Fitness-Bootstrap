<template>
    <section id="landing">
        <div class="container-page">
            <img class="landing-image" src="https://zubayrlatief.github.io/hosted-images/IMG_2337.jpg" alt="image">

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
<style>
.section {
    background-color: #040404;
    max-width: 100%;
    display: flex;
    justify-content: center;
    flex-direction: row;
}



.landing-image {
    width: 35%;
    height: 50%;
    margin-left: 3rem;
    margin-top: 1rem;
}

/*whole page */
.container-page {
    background-color: #040404;
    display: flex;
    justify-items: center;
    flex-direction: row;
    padding: 1.25rem;
}

/* card */
.card {
    width: 20%;
    max-width: 40%;
    height: 10%;
    border-radius: 4px;
    background: #212121;
    display: flex;
    flex-direction: row;
    gap: 5px;
    padding: 0;
    padding-bottom: 0;
    margin-bottom: 0;
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

.card p:hover {
    flex: 4;
}

.card p span {
    min-width: 14em;
    padding: .5em;
    text-align: center;
    transform: rotate(-90deg);
    transition: all .5s;
    text-transform: uppercase;
    color: #ff568e;
    letter-spacing: .1em;
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


</style>