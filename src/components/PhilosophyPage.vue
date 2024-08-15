<template>
    <section id="Philosophy">
        <h1 class="container">OUR PHILOSOPHY</h1>
        <div class="autoShow">
            <img src="https://zubayrlatief.github.io/hosted-images/IMG-20240325-WA0005.jpg" alt=""
                class="autoShow">

            <h2 class="text">
                Our main goal for our clinets
                is to make them succed in progressive,
                incremental and substantaialsteps </h2>

                <h2 class="text-2">
                Our main goal for our clinets<br>
                is to make them succed in progressive,<br>
                infrrrrrrrrrrrrrrrrrrrrrrr</h2>

        </div>
    </section>
</template>
<script>
export default {

}


</script>
<style scoped>
#Philosophy {
    background-color: #040404;


}

.container {
    border: 2px rgb(29, 25, 25) solid;
    color: rgb(193, 189, 185);
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0.75rem;
    font-style: italic;
}

/* Text Section */
.text {
    width: 40%;
    border: 2px black solid;
    display: flex;
    justify-content: end;
    align-items: flex-start;
    margin-top: 6.25rem;
    padding: 1.25rem;
    background-color: rgb(39, 38, 38);
    color: aliceblue;
    font-style: italic;
    font-weight: 200;
}

.text-2 {
    border: 4px black solid;
    height: 50vh;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 4rem;
    background-color: rgb(39, 38, 38);
    color: aliceblue;
    font-style: italic;
    font-weight: 200;
}

/* Auto Show Animation */
.autoShow {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 90vh;
    padding: 1.25rem;
    margin-bottom: 2rem;
    animation: autoShowAnimation both;
    animation-timeline: view(90% 2.5%);
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

/* Responsive Styles */

/* Tablets and smaller screens */
@media (max-width: 1024px) {
    .text {
        width: 60%;
        margin-top: 4rem;
        padding: 1rem;
    }

    .text-2 {
        height: 40vh;
        margin-top: 3rem;
        padding: 1rem;
    }

    .autoShow {
        flex-direction: column;
        height: auto;
        padding: 1rem;
    }
}

/* Phones and smaller screens */
@media (max-width: 768px) {
    .container {
        padding: 0.5rem;
    }

    .text {
        width: 80%;
        margin-top: 3rem;
        padding: 0.75rem;
    }

    .text-2 {
        height: 30vh;
        margin-top: 2rem;
        padding: 0.75rem;
    }

    .autoShow {
        padding: 0.75rem;
    }
}

/* Very small screens (small phones) */
@media (max-width: 480px) {
    .text {
        width: 100%;
        margin-top: 2rem;
        padding: 0.5rem;
    }

    .text-2 {
        height: 20vh;
        margin-top: 1.5rem;
        padding: 0.5rem;
    }

    .autoShow {
        padding: 0.5rem;
    }
}
</style>