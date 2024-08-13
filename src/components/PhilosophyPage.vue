<template>
    <section id="Philosophy">
        <h1 class="container">Our philosophy</h1>
        <div class="autoShow">
            <img src="https://zubayrlatief.github.io/hosted-images/IMG-20240325-WA0005.jpg" alt=""
                class="autoShow">

            <h2 class="text">
                Our main goal for our clinets<br>
                is to make them succed in progressive,<br>
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

.container{
    border: 4px rgb(29, 25, 25) solid;
    color: rgb(193, 189, 185);
    display: flex;
    justify-content: center;
    justify-items: center;
    padding: 1rem;
}


.text{
    width: 40%;
    border: 2px black solid;
    display: flex;
    justify-content: end;
    justify-items: end;
    margin-top: 6.25rem;
    padding: 1.25rem;
    background-color: rgb(39, 38, 38);
    color: aliceblue;
    font-style: italic;
    font-weight: 200;
}

.text-2{
    border: 4px black solid;
    height: 50vh;
    display: flex;
    justify-content: center;
    justify-items: center;
    margin-top: 4rem;
    background-color: rgb(39, 38, 38);
    color: aliceblue;
    font-style: italic;
    font-weight: 200;
}

.autoShow{
    display: flex;
    justify-content: center;
    justify-content: space-between;
    height: 80vh;
    padding: 1.25rem;
    
    animation: autoShowAnimation both;
    animation-timeline: view(90% 2.5%);
}
@keyframes autoShowAnimation{
    from{
        opacity: 0;
        transform: translateY(200px) scale(0.3);
    }to{
        opacity: 1;
        transform: translateY(0) scale(1);
    }
    
}
</style>