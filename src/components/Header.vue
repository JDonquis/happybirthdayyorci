<script setup>
import { onMounted } from 'vue';
import { gsap } from 'gsap';

onMounted(() => {
  gsap.fromTo(".ballons", { x: -300 }, { x: 0, duration: 1 });

});
</script>

<template>
    <header>
        <section class="container header">
            <div class="title">
                <img src="/globos.png" class="ballons" alt="globillos" />
                <h1>¡¡Feliz cumpleaños!!</h1>
                <img src="/globos.png" class="ballons" alt="globillos" />
            </div>
            <span class="gianlugi-subtitle">Gianluigi Strippoli 😎💯</span>
        </section>
    </header>
</template>

<style scoped>

.header{
  padding-top: 5vh;  
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

}

.ballons{

    width: 100px;
    height: 100px;
}

.title{
    display: flex;
    gap: 10px;
    font-size: 32px;
}

.title h1{
    text-align: center;
}

.gianlugi-subtitle
{   
    color: rgba(255, 255, 255, 0.95);
    font-size: 28px;
    font-weight: 800;
    word-spacing: 4px;
    text-align: center;
}

@media (width <= 500px) 
{
    .ballons{

        width: 50px;
        height: 50px;
        }

        .title{
        display: flex;
        gap: 10px;
        font-size: 26px;
        }
}

</style>
