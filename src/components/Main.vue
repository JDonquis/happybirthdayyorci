<script setup>
import { onMounted } from 'vue';
import { gsap } from 'gsap';
import { ref } from 'vue';

const audio = ref(null);

const playAudio = () => {
    audio.value.play();
}

onMounted(() => {
  gsap.fromTo(".photo", { x: -300 }, { x: 0, duration: 1 });
  gsap.fromTo(".text", { x: 300 }, { x: 0, duration: 1 });
});

</script>

<template>
    <main class="container">
        <section class="grid_container_section_main">
            <div class="photo">
                <img src="/yorci.gif" alt="Yorci">
            </div>
            <div class="text">
                <p>
                    Felicidades en tu día Yorci, eres una gran mujer, amiga y prima. Pido al Señor que te siga bendiciendo y que algún día nos podamos volver a ver.
                    Celebro de tenerte un año más en nuestra en vidas. I love you
                    <br>
                    <br>
                    Gracias por estar ahi para apoyarme. <span>I love you</span> 🫶
                </p>
            </div>
            
        
        </section>
    </main>


</template>

<style scoped>

#audio{
    display: none;
}

.grid_container_section_main{
    padding-top:  30px;
    display: grid;
    grid-template-columns: repeat( 2 , 1fr );
    grid-template-rows: auto auto auto;
    gap: 20px;

}
.photo{

    width: min(500px, auto);
    height: min(500px, auto);
    justify-self: right;
}

.photo img{
    width: 100%;
    height: 100%;
    border-radius: 20px;
}

.text{
    padding-top: 15%;
    text-align: left;
    max-width: 530px;
    font-size: 24px;
}

span{
    font-weight: 800;
}

.bible{
    justify-self: center;
    grid-column: 1 / 3;
}

.player{

    justify-self: center;
    grid-column: 1 / 3;
    padding: 10px 12px;
}

@media (width <= 500px) 
{
    .grid_container_section_main{
        padding-top:  30px;
        display: grid;
        grid-template-columns: 1fr;
        grid-template-rows: auto auto auto;
        gap: 20px;
    }

    .text{
        grid-row: 2 / 3;
        text-align: center;
    }

    .bible{
        text-align: center
    }
}

</style>
